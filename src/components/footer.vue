<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; All Rights Reserved {{ currentYear }}</p>
    </div>
  </footer>
</template>

<script>
export default {
  props: {
    currentYear: Number,
  }
};
</script>

<style>
.footer {
  background-color: #8F250C;
  padding: 15px;
  text-transform: capitalize;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 15px;
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  color: #FBBA72;
}
</style>
