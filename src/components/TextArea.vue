<template>
  <div class="text-area">
    <textarea :class="['textarea', type]" :disabled="disabled" :placeholder="placeholder" :readonly="readonly"></textarea>
  </div>
</template>

<script>
export default {
    name: "TextArea",
    props: {
        disabled: false,
        type: String,
        placeholder: String,
        readonly: false
    }
}
</script>

<style scoped>
    .text-area {
        width: 300px;
    }

    .textarea {
        width: 300px;
        height: 200px;
        padding: 20px;
        border: 2px solid #7F5539;
        border-radius: 4px;
        resize: vertical;
        background-color: #f9e7d8;
        color: black;
        font-family: 'Quicksand', sans-serif;
        font-size: 15px;
        box-shadow: 2px 2px 200px rgba(0, 0, 0, 0.1);
        transition: border-color 0.3s ease-in-out;
        margin-top: 10px;
        transition: .5s;
    }
    .areaRound{
        border-radius: 20px;
    }
    .textarea:focus {
        outline: none;
        border-color: #9C6644;
    }

    .textarea::placeholder {
        color: #bf9b85;
    }

    .textarea::-webkit-scrollbar {
        width: 6px;
        background-color: #F5F5F5;
    }

    .textarea::-webkit-scrollbar-thumb {
        background-color: #9C6644;
    }

    .textarea::-webkit-scrollbar-thumb:hover {
        background-color: #7F5539;
    }
    textarea:disabled,
    textarea:disabled ~ textarea::placeholder,
    textarea[disabled]{
        background-color: #c1a595;
        border: solid 3px #ad8d79;
        color: #c1a595,
    }
</style>
