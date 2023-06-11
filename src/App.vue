<template>
  <TabbedNavigation webTitle="Slap Soil">
    <Tabs title="Home">
        <Greetings />
    </Tabs>

    <Tabs title="Button">
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
  
  <Footer currentYear ="2023"/>
</template>

<script>
import Tabs from './components/navTabs.vue'
import TabbedNavigation from './components/TabbedNavigation.vue'
import Greetings from './componentTabs/HomeGreeting.vue'
import ButtonComponentTab from './componentTabs/ButtonComponent.vue'
import LineComponentTab from './componentTabs/LineComponent.vue'
import CheckboxComponentTab from './componentTabs/CheckboxComponent.vue'
import RadioButtonComponentTab from './componentTabs/RadioButtonComponent.vue'
import RadioButtonGroupComponentTab from './componentTabs/RadioButtonGroupComponent.vue'
import TabContainerComponentTab from './componentTabs/TabContainerComponent.vue'
import Footer from './components/footer.vue'


export default{
  name: 'App',
  components: {
    Tabs,
    TabbedNavigation,
    Greetings,
    ButtonComponentTab,
    LineComponentTab,
    CheckboxComponentTab,
    RadioButtonComponentTab,
    RadioButtonGroupComponentTab,
    TabContainerComponentTab,
    Footer
  },
}
</script>

<style scoped>

</style>
