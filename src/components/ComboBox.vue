<template>
  <div class="combo-box">
    <select :class="['select-box', disabled? 'disabled': '']" :disabled="disabled">
      <option v-for="option in options" :key="option.value" :value="option.value">{{ option.label }}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'ComboBox',
  props: {
    options: {
      type: Array,
      required: true,
    },
    disabled: false,
  }
};
</script>

<style scoped>
.combo-box {
  display: flex;
  align-items: center;
}

.select-box {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  background-color: #9C6644;
  color: white;
  font-family: Arial, sans-serif;
  font-size: 20px;
  line-height: 1.5;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
  width: 200px;
}

.select-box:hover {
  background-color: #7F5539;
}

.disabled:hover{
  background-color: #9C6644;
}

.selected-option {
  margin-left: 8px;
  color: #9C6644;
  font-size: 16px;
  font-weight: bold;
}
</style>
