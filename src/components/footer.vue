<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; {{ currentYear }}</p>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: 'All Rights Reserved 2023',
    };
  },
};
</script>

<style>
.footer {
  background-color: #d4a373;
  padding: 15px;
  text-transform: capitalize;
  text-align: center;
  font-size: 20px;
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  color: #780116;
}
</style>
