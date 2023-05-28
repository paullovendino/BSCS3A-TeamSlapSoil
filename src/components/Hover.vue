<template>
  <div class="Hover">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Hover',
  props: {
    type: String,
  },
}
</script>

<style scoped>
.Hover {
  cursor: pointer;
  font-size: 20px;
}

.Hover:hover {
  background-color: #EDE0D4;
  color: #7F5539;
}
</style>
