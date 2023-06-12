<template>
  <div class="avatar">
    <img :src="imageUrl" :alt="altText" class="avatar-image">
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
      default: 'Avatar'
    },
    resizeOption: {
      type: String,
      default: '100px' // default resize option value
    }
  }
};
</script>

<style scoped>
.avatar {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  overflow: hidden;
  background-color: #E6CCB2;
}

.avatar-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
