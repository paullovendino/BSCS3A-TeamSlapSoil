<template>
  <div class="radio-group">
    <h3>{{ title }}</h3>
    <label v-for="option in options" :key="option.value" class="radio-label">
      <input type="radio" v-model="selectedOption" :value="option.value" :name="name" :id="options.label" class="radio-input" :disabled="disabled">
      <span class="radio-text" :for="options.label">{{ option.label }}</span>
    </label>
  </div>
</template>

<script>
export default {
  props: {
    options: {
      type: Array,
      required: true
    },
    disabled: false,
    title: String,
    name: String,
  },
  data() {
    return {
      selectedOption: ''
    }
  }
}
</script>

<style scoped>
.radio-group {
  display: flex;
  flex-direction: column;
  border: 2px solid #67432c;
  padding: 10px
}

.radio-label {
  display: flex;
  align-items: center;
  font-size: 16px;
  margin-bottom: 8px;
}

.radio-input {
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  width: 16px;
  height: 16px;
  border: 2px solid #ccc;
  border-radius: 50%;
  outline: none;
  margin-right: 8px;
  cursor: pointer;
}

.radio-text {
  color: #9C6644;
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
input:disabled ~ .radio-text,
input[type="radio"][disabled]{
    cursor: default;
    color: #f4cca1 !important;
}
input:disabled ~ .radio-icon,
input[type="radio"][disabled]{
    background-color: #f4d9bd;
    border-color: #f8d6b1;
}
.radio-group h3{
  color: #67432c;
  margin: 0 10px 10px 10px;
}

</style>
