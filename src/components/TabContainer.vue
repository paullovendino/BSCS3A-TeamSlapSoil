<template>
    <div class="tabs">
        <div class="title" v-if="Container_Title != ''">
            <h3>{{ Container_Title }}</h3>
        </div>

        <ul class="tabs_header">
            <li v-for="title in tabTitles" 
            :class="{ selected: title==selectedTitle}"
            :key="title" 
            @click="selectedTitle = title">
                {{ title }}
            </li>
        </ul>
        <div class="tab_content">
            <slot></slot>
        </div>
    </div>
</template>

<script>
    import { ref, provide } from 'vue'

    export default {
        name: 'TabContainer',
        data(){
            return{

            }
        },
        props: {
            Container_Title: String,
        },
        setup(props, { slots }){
            const tabTitles = ref(slots.default().map((tab) => tab.props.title))
            const selectedTitle = ref(tabTitles.value[0])

            provide('selectedTitle', selectedTitle)

            return{
                selectedTitle,
                tabTitles,
            }
        }
    }
</script>

<style scoped>
.tabs{
    max-width: 400px;
    margin: 0 auto;
    text-align: center;
}

.tabs_header{
    margin-bottom: 5px;
    list-style: none;
    padding: 0;
    display: flex;
}

.tabs_header li{
    min-width: 50px;
    padding: 10px 20px;
    text-align: center;
    margin-right: 10px;
    background-color: #B08968;
    color: #E6CCB2;
    border-radius: 20px;
    cursor: pointer;
    transition: 0.4s all ease-out;
}

.tabs_header li.selected{
    background-color: #7F5539;
    color: #EDE0D4;
}

.tabs_header li:hover{
    background-color: #7b5e4b;
    color: #EDE0D4;
}

.tabs_header li:active{
    background: #B08968;
    color: #E6CCB2;
    box-shadow: 1px 1px rgb(0, 0, 0, 0.5);
    transition: 0s;
}

.tab_content{
    min-height: 150px;
    border: 2px solid #7F5539;
    border-radius: 20px;
    box-shadow: 0 2px 2px 2px rgb(0, 0, 0, 0.5);
}

.title{
    margin: 15px;
    color: #7b5e4b;
    font-weight: 700;
    font-size: x-large;
}
</style>