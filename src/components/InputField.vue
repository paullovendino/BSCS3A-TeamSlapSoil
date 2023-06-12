<template>
  <div class="input">
    <input :class="['inputField', type]" type="text" placeholder="Enter text" :disabled="disabled">
  </div>
</template>

<script>
export default {
        name: 'InputField',
        props: {
            disabled: false,
            type: String
        }
  }


</script>

<style>
    .inputField{
        height: 30px;
        border: solid 3px #b08968;
        padding-left: 8px;
        font-family: 'Quicksand', sans-serif;
        font-size: 15px;
        transition: .5s;
    }
    .inputRound{
        border-radius: 20px;
    }
    input:disabled,
    input[disabled]{
        background-color: rgb(216, 216, 216);
        border: solid 3px gray;
    }


</style>
