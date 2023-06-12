<template>
  <div class="avatar">
    <img :src="imageUrl" :alt="alt" class="avatar-image">
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
      default: 'Avatar'
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
