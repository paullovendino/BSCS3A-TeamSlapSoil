<template>
  <TabbedNavigation webTitle="Slap Soil" sidebarTitle="Components">
    <Tabs title="Home">
        <div class="container">
            <Greetings/>
        </div>
    </Tabs>
    <Tabs title="Component 1"><Template /></Tabs>
    <Tabs title="Component 2"></Tabs>
    <Tabs title="Component 3"></Tabs>
    <Tabs title="Component 4"></Tabs>
    <Tabs title="Component 5"></Tabs>
    <Tabs title="Component 6"></Tabs>
    <Tabs title="Component 7"></Tabs>
    <Tabs title="Component 8"></Tabs>
    <Tabs title="Component 9"></Tabs>
  </TabbedNavigation>
</template>

<script>
import Tabs from './components/navTabs.vue'
import TabbedNavigation from './components/TabbedNavigation.vue'
import Greetings from './components/HomeGreeting.vue'
import Template from './components/Content-Template.vue'


export default{
  name: 'App',
  components: {
    Tabs,
    TabbedNavigation,
    Greetings,
    Template
  },
  data (){
    return{
      
    }
  }
}
</script>

<style scoped>

</style>
