<template>
  <div class="combo-box" :disabled="disabled">
    <select v-model="selectedOption" class="select-box">
      <option v-for="option in options" :key="option.value" :value="option.value">{{ option.label }}</option>
    </select>
    <span class="selected-option">Selected option: {{ selectedOption }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedOption: '',
      options: [
        { value: 'London', label: 'London' },
        { value: 'Paris', label: 'Paris' },
        { value: 'New York', label: 'New York' },
        { value: 'Milan', label: 'Milan' }
      ]
    };
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

.selected-option {
  margin-left: 8px;
  color: #9C6644;
  font-size: 16px;
  font-weight: bold;
}
</style>
