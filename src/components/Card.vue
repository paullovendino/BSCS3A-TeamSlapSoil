<template>
    <div :class="type" id="wrapper">
        <div class="content">
            <h2 v-if="title != '' ">{{ title }}</h2>
            <h4 v-if="subTitle != ''">{{ subtitle }}</h4>
            <hr v-if="title != '' || subTitle != ''"/>
            <slot></slot>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Card',
        props: {
            type: String,
            title: String,
            subtitle: String,
        }
    }
</script>

<style scoped>
    #wrapper{
        background: #E6CCB2;
        color: #7F5539;
        box-shadow: 0 3px 5px 5px rgb(0, 0, 0, 0.5);
        width: fit-content;
        max-width: 400px;
        height: auto;
    }

    .content{
        padding: 20px;
    }

    .outlined{
        border: 2px solid black;
        box-shadow: none !important;
    }

    .tonal{
        background: #EDE0D4;
        box-shadow: none !important;
    }

    h2{
        font-weight: 500;
    }

    h4{
        opacity: 0.8;
    }

    hr{
        background: #7F5539;
        color: #7F5539;
        border: none;
        height: 1px;
        margin-bottom: 15px;
    }
    
</style>
