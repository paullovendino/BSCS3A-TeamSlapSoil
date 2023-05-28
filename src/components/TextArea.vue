<template>
  <div class="text-area">
    <textarea v-model="text" class="textarea"></textarea>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'This is a textbox'
    }
  }
}
</script>

<style scoped>
.text-area {
  width: 300px;
}

.textarea {
  width: 100%;
  height: 150px;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
  resize: vertical;
  background-color: #7F5539;
  color: white;
}
</style>
