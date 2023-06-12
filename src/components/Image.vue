<template>
  <div class="image-component-wrapper">
    <div class="image-wrapper">
        <img src="https://media.istockphoto.com/id/1096052566/vector/stamprsimp2red.jpg?s=612x612&w=0&k=20&c=KVu0nVz7ZLbZsRsx81VBZcuXZ1MlEmLk9IQabO2GkYo=" :alt="altText" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imageUrl: {
      type: String,
      required: true
    },
    altText: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
    .image-component-wrapper{
        display: flex;
    }
    .image-wrapper{
        display: flex;
        height: 300px;
        align-items: center;
        justify-content: center;
    }
</style>
