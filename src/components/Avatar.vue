<template>
  <div :class="[size, 'avatar']">
    <img :src="imageUrl" :alt="alt" class='avatar-image'>
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
    },
    size: String,
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

div{
  width: 50px
}

.xx-small{
  width: 20px;
}

.x-small{
  width: 30px;
}

.medium{
  width: 80px;
}

.large{
  width: 120px;
}

.x-large{
  width: 160px;
}

.xx-large{
  width: 200px;
}

</style>
