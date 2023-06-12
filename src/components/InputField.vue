<template>
  <div>
    <input type="text" :class="type" :placeholder="placeholder" :readonly="readonly" :disabled="disabled">
  </div>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: "input-field",
    },
    placeholder: '',
    readonly: false,
    disabled: false,
  }
};
</script>

<style>
input{
  background-color: #E6CCB2;
  padding: 10px;
  border: 1px solid #7F5539;
  border-radius: 4px;
  outline: #7F5539;
}

.dark {
  background-color: #7F5539;
  padding: 10px;
  border: 1px solid #E6CCB2;
  border-radius: 4px;
  outline: #E6CCB2;
  color: white;
}

.underlined-light {
  border: none;
  border-bottom: 1px solid #E6CCB2;
  outline: none;
}

.underlined-dark {
  border: none;
  border-bottom: 1px solid #7F5539;
  outline: none;
}

.outlined-light {
  outline: 1px solid #E6CCB2;
}

.outlined-dark {
  outline: 1px solid #7F5539;
}

.solo {
  background-color: transparent;
  border: none;
  outline: none;
}

.solo-filled {
  background-color: #E6CCB2;
  border: none;
  outline: none;
}

.solo-inverted {
  background-color: #7F5539;
  color: #E6CCB2;
  border: none;
  outline: none;
}

input[type="text"]::placeholder{
  color: #9f6e3d
}

input:disabled,
input:disabled ~ input::placeholder,
input[type = "text"][disabled]{
  background: #cab29d;
  border-color: #a58d75;
}
</style>
