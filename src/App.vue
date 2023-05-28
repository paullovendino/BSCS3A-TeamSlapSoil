<script>
import MySwitch from './components/MySwitch.vue'
import Image from './components/Image.vue'

export default{
  name: 'App',
  components: {
    MySwitch,
    Image
  },
  data (){
    return{
      switchValue: false
    }
  }
}
</script>

<template>
  <header>
    <div class="wrapper">
      <MySwitch :switch-value="switchValue" @switchValueChanged="switchValue = !switchValue"></MySwitch>
      <Image :imageUrl="'https://www.positivethinking.tech/wp-content/uploads/2021/01/Logo-Vuejs.png'"></Image>
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
