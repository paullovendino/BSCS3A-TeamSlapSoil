<script>
import HelloWorld from './components/HelloWorld.vue'

export default{
  name: 'App',
  components: {
    HelloWorld,
  }
}
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="Just a Sample Program" />
    </div>
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
