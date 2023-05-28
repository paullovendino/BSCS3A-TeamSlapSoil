<template>
  <div class="image-component-wrapper">
    <div class="image-wrapper">
        <img :src="imageUrl" :alt="altText" />
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