<template>
    <div class="combo-box">
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
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
    background-color: #9C6644;
    color: white;
  }
  
  .selected-option {
    margin-left: 8px;
    color: brown;
  }
  </style>
  