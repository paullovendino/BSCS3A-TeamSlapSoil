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
  width: 500px;
  height: 200px;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
  resize: vertical;
  background-color: #7F5539;
  color: white;
  font-family: Arial, sans-serif;
  font-size: 20px;
  line-height: 1.5;
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
  transition: border-color 0.3s ease-in-out;
  margin-top: 10px;
}

.textarea:focus {
  outline: none;
  border-color: #9C6644;
}

.textarea::placeholder {
  color: #ccc;
}

.textarea::-webkit-scrollbar {
  width: 6px;
  background-color: #F5F5F5;
}

.textarea::-webkit-scrollbar-thumb {
  background-color: #9C6644;
}

.textarea::-webkit-scrollbar-thumb:hover {
  background-color: #7F5539;
}
</style>
