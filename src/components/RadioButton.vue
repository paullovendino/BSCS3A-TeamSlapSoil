<template>
    <div>
        <input type="radio" :name="name" :value="value" :id="id" @click="$emit('valueChanged', $event.target.value)"/>
        <label class="radio-label" :for="name">
            {{ label }}
        </label>
    </div>
</template>

<script>
    export default {
        props: {
            name: String,
            value: String,
            label: String,
            id: String,
        }
    }
</script>

<style scoped>
    div{
        display: flex;
        align-items: center;
    }

    .radio-label {
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 15px;
        color: #7F5539;
    }

    input[type="radio"]{
        -webkit-appearance: none;
        -moz-appearance: none;
        width: 14px;
        height: 14px;
        border: 2px solid brown;
        border-radius: 4px;
        outline: none;
        position: relative;
        margin-right: 4px;
        cursor: pointer;
    }

    input[type="radio"]:checked {
        background-color: brown;
        border-color: #DDB892;
    }

    input[type="radio"]:checked::after {
        content: "\2713";
        display: block;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 12px;
        color: white;
    }
</style>