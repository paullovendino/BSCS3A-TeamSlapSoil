<template>
  <div class="image-wrapper">
    <img :src="imageUrl" :alt="alt" />
  </div>
</template>

<script>
export default {
  props: {
    imageUrl: {
      type: String,
      required: true
    },
    alt: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
    .image-wrapper{
      width: 100%;
      height: 100%
    }

    img{
      height: 100%;
      width: 100%;
      object-fit: cover;
    }
</style>
