<template>
    <div>
        <button :class="[size, type]" :disabled="disabled">
            <p>{{ text }}</p>
        </button>
    </div>
</template>

<script>
    export default {
        name: 'btnSoil',
        props: {
            text: String,
            size: String,
            disabled: false,
            type: String,
        }
    }
</script>

<style scoped>
    .xx-small{
        font-size: xx-small;
        height: 25px;
    }

    .x-small{
        font-size: x-small;
        height: 30px;
    }
    
    .medium{
        font-size: medium;
    }

    .large{
        font-size: large;
    }

    .x-large{
        font-size: x-large;
    }

    .xx-large{
        font-size: xx-large;
    }

    button{
        background: #B08968;
        color: #E6CCB2;
        padding: 10px;
        border: none;
        box-shadow: 2px 2px rgb(0, 0, 0, 0.5);
        cursor: pointer;
    }
    
    button:hover{
        background: #7F5539;
        color: #EDE0D4;
        box-shadow: 3px 3px rgb(0, 0, 0, 0.5);
    }

    button:active{
        background: #B08968;
        color: #E6CCB2;
        box-shadow: 2px 2px rgb(0, 0, 0, 0.5);
        transition: 0s;
    }

    button:disabled,
    button[disabled]{
        background: #E6CCB2;
        color: #EDE0D4;
        box-shadow: 2px 2px rgb(0, 0, 0, 0.5);
        cursor: default;
    }

    .outlined{
        border: 1px solid black;
        box-shadow: none;
    }

    .outlined:hover{
        border: 1px solid black;
        box-shadow: none;
    }

    .outlined:active{
        border: 1px solid black;
        background: #B08968;
        color: #E6CCB2;
        box-shadow: none;
        transition: 0s;
    }

    .outlined:disabled,
    .outlined[disabled]{
        background: #E6CCB2;
        color: #EDE0D4;
        box-shadow: none;
    }

    .text{
        background: none;
        box-shadow: none;
        color: #7F5539;
    }

    .text:hover{
        box-shadow: none;
        color: #7F5539;
        background: #e9c9ab;
    }

    .text:active{
        background: none;
        box-shadow: none;
        color: #7F5539;
        transition: 0s;
    }

    .text:disabled,
    .text[disabled]{
        color: #E6CCB2;
        background: none;
        box-shadow: none;
    }

    .tonal{
        box-shadow: none;
        color: #392415;
        background: #E6CCB2;
    }

    .tonal:hover{
        background: #B08968;
        color: #392415;
        box-shadow: none;
    }

    .tonal:active{
        box-shadow: none;
        color: #392415;
        background: #E6CCB2;
        transition: 0s;
    }

    .tonal:disabled,
    .tonal[disabled]{
        background: #E6CCB2;
        color: #EDE0D4;
        box-shadow: none;
    }

    .plain{
        background: none;
        box-shadow: none;
        color: #B08968;
    }

    .plain:hover{
        background: none;
        box-shadow: none;
        color: #392415;
    }

    .plain:active{
        background: none;
        box-shadow: none;
        color: #B08968;
        transition: 0s;
    }

    .plain:disabled,
    .plain[disabled]{
        color: #E6CCB2;
        background: none;
        box-shadow: none;
    }
</style>
