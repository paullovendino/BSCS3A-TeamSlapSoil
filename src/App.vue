<template>
  <TabbedNavigation webTitle="Slap Soil">
    <Tabs title="Home">
        <Greetings />
    </Tabs>

    <Tabs title="Button Component">
      <ButtonComponentTab/>
    </Tabs>
    
    <Tabs title="Line/Divider Component">
      <LineComponent/>
    </Tabs>

    <Tabs title="Switch Component">
      <SwitchComponent/>
    </Tabs>
    <Tabs title="Input Field Component">
      <InputFieldComponent/>
    </Tabs>

    <Tabs title="Text Area Component">
      <TextAreaComponent/>
    </Tabs>

    <Tabs title="Avatar Component">
      <AvatarComponent/>
    </Tabs>

    <Tabs title="Hover Component">
      <HoverComponent/>
    </Tabs>

    <Tabs title="Expansion Panel Component">
      <ExpansionPanelComponent />
    </Tabs>

    <Tabs title="ComboBox Component">
      <ComboBoxComponent/>
    </Tabs>
    <Tabs title="Image Component">
      <ImageComponent/>
    </Tabs>
    <Tabs title="AppBar Component">
      <AppBarComponent/>
    </Tabs>
    <Tabs title="BreadCrumb Component">
      <BreadCrumbComponent/>
    </Tabs>
  </TabbedNavigation>
</template>

<script>
import Tabs from './components/navTabs.vue'
import TabbedNavigation from './components/TabbedNavigation.vue'
import Greetings from './componentTabs/HomeGreeting.vue'
import ButtonComponentTab from './componentTabs/ButtonComponent.vue'
import LineComponent from './componentTabs/LineComponent.vue'
import SwitchComponent from './componentTabs/SwitchComponent.vue'
import InputFieldComponent from './componentTabs/InputFieldComponent.vue'
import TextAreaComponent from './componentTabs/TextAreaComponent.vue'
import AvatarComponent from './componentTabs/AvatarComponent.vue'
import HoverComponent from './componentTabs/HoverComponent.vue'
import ExpansionPanelComponent from './componentTabs/ExpansionPanelComponent.vue'
import ComboBoxComponent from './componentTabs/ComboBoxComponent.vue'
import ImageComponent from './componentTabs/ImageComponent.vue'
import AppBarComponent from './componentTabs/AppBarComponent.vue'
import BreadCrumbComponent from './componentTabs/BreadCrumbComponent.vue'


export default{
  name: 'App',
  components: {
    Tabs,
    TabbedNavigation,
    Greetings,
    ButtonComponentTab,
    LineComponent,
    SwitchComponent,
    InputFieldComponent,
    TextAreaComponent,
    AvatarComponent,
    HoverComponent,
    ExpansionPanelComponent,
    ComboBoxComponent,
    ImageComponent,
    AppBarComponent,
    BreadCrumbComponent
  },
}
</script>

<style scoped>

</style>
