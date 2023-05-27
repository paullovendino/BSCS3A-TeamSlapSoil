<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <h3>{{ msg }}</h3>
</template>

<style scoped>
h3 {
  font-size: 1.2rem;
}
</style>
