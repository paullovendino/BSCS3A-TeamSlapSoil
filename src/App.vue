<script>
import HelloWorld from './components/HelloWorld.vue'
import MySwitch from './components/MySwitch.vue'

export default{
  name: 'App',
  components: {
    HelloWorld,
    MySwitch
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
      <HelloWorld msg="Just a Sample Program" />
      <MySwitch :switch-value="switchValue" @switchValueChanged="switchValue = !switchValue"></MySwitch>
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
