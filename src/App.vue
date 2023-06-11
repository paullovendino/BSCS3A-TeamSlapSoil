<template>
  <TabbedNavigation webTitle="Slap Soil">
    <Tabs title="Home">
        <div class="container">
            <Greetings/>
        </div>
    </Tabs>

    <Tabs title="Button Component">
      <ButtonComponentTab/>
    </Tabs>
    
    <Tabs title="Component 2">

    </Tabs>

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
import ButtonComponentTab from './componentTabs/ButtonComponent.vue'


export default{
  name: 'App',
  components: {
    Tabs,
    TabbedNavigation,
    Greetings,
    ButtonComponentTab,
  },
}
</script>

<style scoped>
  
</style>
