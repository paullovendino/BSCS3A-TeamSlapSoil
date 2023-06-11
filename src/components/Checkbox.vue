<template>
  <div>
    <label class="checkbox-label">
      <input type="checkbox" v-model="selectedItems">
      {{ label }}
    </label>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const props = defineProps({
  label: {
    type: String,
    default: 'item' 
  }
});

const selectedItems = ref(false);

const displayedItem = computed(() => props.label);

</script>

<style scoped>
.checkbox-label {
  display: flex;
  align-items: center;
  font-size: 15px;
  margin-bottom: 8px;
  color: #9C6644;
}

input[type="checkbox"] {
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  width: 14px;
  height: 14px;
  border: 2px solid brown;
  border-radius: 4px;
  outline: none;
  vertical-align: middle;
  position: relative;
  top: 2px;
  margin-right: 4px;
  cursor: pointer;
}

input[type="checkbox"]:checked {
  background-color: brown;
  border-color: #DDB892;
}

input[type="checkbox"]:checked::after {
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
