<template>
    <div>
        <button :class="[size, type, disabled ? 'disabled' : '']" :disabled="disabled">
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
            disabled: {
                type: Boolean,
                default: false
            },
            type: {
                type: String,
            }
        }
    }
</script>

<style scoped>
    .xx-small{
        font-size: xx-small;
        width: 75px;
        height: 30px
    }

    .x-small{
        font-size: x-small;
        width: 80px;
        height: 30px
    }
    .medium{
        font-size: medium;
        width: 120px;
        height: 50px
    }

    .large{
        font-size: large;
        width: 140px;
        height: 60px
    }

    .x-large{
        font-size: x-large;
        width: 175px;
        height: 75px
    }

    .xx-large{
        font-size: xx-large;
        width: 225px;
        height: 95px
    }

    button{
        background: #B08968;
        color: #E6CCB2;
        padding: 10px;
        border: none;
        box-shadow: 2px 2px rgb(0, 0, 0, 0.5);
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
    }

    .disabled{
        pointer-events: none;
    }

    .disabled:hover{
        pointer-events: none;
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
    }

    .text{
        background: none;
        box-shadow: none;
        color: #7F5539;
    }

    .text:hover{
        box-shadow: none;
        color: #7F5539;
        background: #EDE0D4;
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
    }
</style>
