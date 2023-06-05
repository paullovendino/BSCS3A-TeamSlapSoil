<template>
    <div class="navbar">
        <input type="checkbox" v-model="checked" id="check">
        <label for="check">
            <div :class="[checked? 'checkedIconShow': '', 'menu-button']" id="show">
                <div class="menu-icon">
                    <div class="line"></div>
                    <div class="line"></div>
                    <div class="line"></div>
                </div>
            </div>

            <div :class="[checked? 'checkedIconCancel': '', 'menu-button']" id="cancel">
                <h2>X</h2>
            </div>
        </label>

        <div class="webTitle">
            <h3>{{webTitle}}</h3>
        </div>
    </div>

    <div :class="[checked? 'checked' : 'unchecked' ,'sidebar']">
        <header>{{ sidebarTitle }}</header>
        <ul class="tab_header">
            <li v-for="title in tabTitles" :key="title" 
            @click="selectedTitle = title" 
            :class="selectedTitle == title? 'active': '' ">
                <p>{{ title }}</p>    
            </li>
        </ul>
    </div>

    <div :class="checked? 'contentChecked': '' ">
        <slot>

        </slot>
    </div>
</template>

<script>
    import { ref, provide } from 'vue'

    export default {
        data(){
            return{
                checked: false,
            }
        },
        props: {
            webTitle: String,
            sidebarTitle: String,
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
    .checked{
        left: 0px;
    }

    .unchecked{
        left: -250px
    }

    .checkedIconShow{
        left: 250px;
        opacity: 0;
        pointer-events: none;
    }

    .contentChecked{
        margin-left: 250px;
    }
    
    .checkedIconCancel{
        left: 180px !important;
    }
    
    .sidebar::-webkit-scrollbar{
        width: 10px;
    }

    .sidebar::-webkit-scrollbar-thumb{
        background-color: #FBBA72;
    }

    .sidebar::-webkit-scrollbar-track{
        background-color: #8F250C;
    }
    
    .navbar{
        display: flex;
        background: #8F250C;
        width: 100%;
        height: 80px;
        align-items: center;
        justify-content: space-between;
    }
    
    .sidebar{
        position: fixed;
        width: 250px;
        height: 100%;
        background: #8F250C;
        overflow-y: scroll;
        transition: all .5s ease;
        padding-bottom: 60px;
    }

    .sidebar ul{
        padding-inline-start: 0 !important;
    }

    .sidebar li{
        display: block;
        list-style: none;
        height: 100%;
        width: 100%;
        padding-top: 30px;
        padding-bottom: 20px;
        margin-left: 10px;
        font-size: 15px;
        color: white;
        box-sizing: border-box;
        border-top: 1px solid rgba(255, 255, 255, .1);
        border-bottom: 1px solid black;
        transition: .1s ease;
    }

    .sidebar li p{
        margin-left: 20px;
    }

    ul li:hover{
        padding-left: 15px;
        color: #FBBA72;
    }

    ul li.active{
        padding-left: 15px;
        background: #551102;
        color: #FBBA72;
    }

    .sidebar header{
        font-size: 25px;
        color: white;
        text-align: center;
        line-height: 70px;
        background: #8F250C;
        user-select: none;
    }

    .webTitle h3{
        color: #FBBA72;
        margin-right: 90px;
        font-size: 40px;
        font-weight: 700;
    }
    
    .menu-button {
        cursor: pointer;
        background: none;
        border: none;
        padding: 0;
        margin-left: 30px;
    }
  
    .menu-icon {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: 25px;
        height: 20px;
    }

    .menu-button h2{
        color: #FBBA72;
        font-weight: 800;
    }
    
    .line {
        width: 100%;
        height: 4px;
        background-color: #FBBA72;
    }

    #check{
        display: none;
    }

    #show, #cancel{
        position: absolute;
        cursor: pointer;
        background: #8F250C;
        border-radius: 3px;
    }

    #show{
        top: 25px;
        font-size: 35px;
        color: #FBBA72;
        padding: 6px 12px;
        transition: all .4s;
    }

    #cancel{
        z-index: 1000;
        left: -180px;
        top: 17px;
        color: #FBBA72;
        padding: 4px 9px;
        transition: all .5s ease;
    }
</style>
