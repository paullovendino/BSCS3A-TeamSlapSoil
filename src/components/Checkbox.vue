<template>
  <div>
    <input
      type="checkbox" :name="name" :value="value" :id="id" :checked="checked" :disabled="disabled" @change="updateStatus" :ref="disabled ? 'disabledButton' : ''"/>
    <label class="checkbox-label" :for="id">
      <span class="checkbox-icon"></span>
      {{ label }}
    </label>
  </div>
</template>

<script>
export default {
  name: 'Checkbox',
  props: {
    name: String,
    value: String,
    label: String,
    id: String,
    checked: {
      type: Boolean,
      default: false
    },
    disabled: {
      type: Boolean,
      default: true
    }
  },
  methods: {
    updateStatus(event) {
      const isChecked = event.target.checked;
      this.$emit('update:checked', isChecked);
    }
  }
};
</script>


<style scoped>
.checkbox-label {
  display: flex;
  align-items: center;
  font-size: 20px;
  margin-bottom: 8px;
  color: #9C6644;
}

.checkbox-icon {
  display: inline-block;
  width: 16px;
  height: 16px;
  border: 2px solid brown;
  border-radius: 4px;
  position: relative;
  top: 2px;
  margin-right: 4px;
}

input[type="checkbox"] {
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  width: 16px;
  height: 16px;
  outline: none;
  vertical-align: middle;
  position: relative;
  margin-right: 4px;
  cursor: pointer;
}

input[type="checkbox"]:checked + .checkbox-label .checkbox-icon {
  background-color: brown;
  border-color: #DDB892;
}

input[type="checkbox"]:checked + .checkbox-label .checkbox-icon::after {
  content: "\2713";
  display: block;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 12px;
  color: white;
}

input[type="checkbox"]:disabled + .checkbox-label .checkbox-icon {
  background-color: #E6CCB2;
  border-color: #E6CCB2;
}

input[type="checkbox"]:disabled + .checkbox-label {
  color: #E6CCB2;
}
</style>
