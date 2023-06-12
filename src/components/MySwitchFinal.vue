<template>
    <div class="switch">
        <label>
            <input type="checkbox" :checked="checked" :disabled="disabled">
            <span :class="['slider', type]"></span>
        </label>
    </div>
</template>

<script>
export default {
        name: 'Switch',
        props: {
            checked: false,
            disabled: false,
            type: String
        }
}
</script>

<style>
    .switch{
    position: relative;
    display: inline-block;
    width: 60px;
    height: 34px;
    color: black;
    }

    .switch input {
    opacity: 0;
    width: 0;
    height: 0;
    }

    .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: gray;
    -webkit-transition: .4s;
    transition: .4s;
    }

    .slider:before {
    position: absolute;
    content: "";
    height: 26px;
    width: 26px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: .4s;
    transition: .4s;
    }

    input:checked + .slider {
    background-color: #7F5539;
    }

    input:focus + .slider {
    box-shadow: 0 0 1px #7F5539;
    }

    input:checked + .slider:before {
    -webkit-transform: translateX(26px);
    -ms-transform: translateX(26px);
    transform: translateX(26px);
    }

    /* Rounded sliders */
    .round{
        border-radius: 34px;
    }
    .round:before {
        border-radius: 50%;
    }
    input:disabled ~ .slider,
    input[disabled]{
        background-color: lightgray;
    }
    input:disabled ~ .slider:before,
    input[disabled]{
        background-color: rgb(189, 189, 189);
    }
</style>
