<template>
  <div>
        <input type="checkbox" :name="name" :value="value" :id="id" @change="$emit('isChecked', $event.target.checked)" :checked="checked" :disabled="disabled"/>
        <label class="checkbox-label" :for="name">
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
        disabled: {
          type: Boolean,
          default: false,
        },
        checked: {
          type: Boolean,
          default: false,
        }
    }
  }
</script>

<style scoped>
div{
  display: flex;
  align-items: center;
}

.checkbox-label {
  display: flex;
  align-items: center;
  font-size: 15px;
  color: #7F5539;
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

input:disabled ~ .checkbox-label,
input[type="checkbox"][disabled]{
  cursor: default;
  color: #f4d9bd !important;
}

input:disabled ~ .checkbox-icon,
input[type="checkbox"][disabled]{
  background-color: #f4d9bd;
  border-color: #f8d6b1;
}

</style>
