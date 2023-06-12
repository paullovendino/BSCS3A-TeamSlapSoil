<template>
  <div class="text-area">
    <textarea v-model="text" :class="['textarea', type]" :disabled="disabled"></textarea>
  </div>
</template>

<script>
export default {
    name: "TextArea",
    props: {
        disabled: false,
        type: String
    },
    data() {
      return {
        text: 'This is a Text Area'
      }
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
        padding: 8px;
        border: 2px solid #b08968;
        border-radius: 4px;
        resize: vertical;
        background-color: white;
        color: black;
        font-family: 'Quicksand', sans-serif;
        font-size: 18px;
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
        color: #ccc;
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
    textarea[disabled]{
        background-color: rgb(216, 216, 216);
        border: solid 3px gray;
    }
</style>
