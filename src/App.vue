<template>
  <TabbedNavigation webTitle="Slap Soil">
    <Tabs title="Home">
        <Greetings />
    </Tabs>

    <Tabs title="Button Component">
      <ButtonComponentTab/>
    </Tabs>
    
    <Tabs title="Line/Divider Component">
      <LineComponentTab/>
    </Tabs>

    <Tabs title="Switch Component">
      <SwitchComponentTab/>
    </Tabs>

    <Tabs title="Input Field Component">
      <InputFieldComponentTab/>
    </Tabs>

    <Tabs title="Text Area Component">
      <TextAreaComponentTab/>
    </Tabs>

    <Tabs title="Avatar Component">
      <AvatarComponentTab/>
    </Tabs>

    <Tabs title="Hover Component">
      <HoverComponentTab/>
    </Tabs>

    <Tabs title="Expansion Panel Component">
      <ExpansionPanelComponentTab />
    </Tabs>

    <Tabs title="ComboBox Component">
      <ComboBoxComponentTab/>
    </Tabs>

    <Tabs title="Image Component">
      <ImageComponentTab/>
    </Tabs>

    <Tabs title="AppBar Component">
      <AppBarComponentTab/>
    </Tabs>

    <Tabs title="BreadCrumb Component">
      <BreadCrumbComponentTab/>
    </Tabs>

    <Tabs title="Checkbox Component">
      <CheckboxComponentTab/>
    </Tabs>

    <Tabs title="Radiobutton Component">
      <RadioButtonComponentTab/>
    </Tabs>

    <Tabs title="Radiobutton Group Component">
      <RadioButtonGroupComponentTab/>
    </Tabs>

    <Tabs title="Card Component">
      <CardComponentTab/>
    </Tabs>

    <Tabs title="Tabs Component">
      <TabContainerComponentTab/>
    </Tabs>

  </TabbedNavigation>
  
  <Footers currentYear = "2023" />
</template>

<script>
import Tabs from './components/navTabs.vue'
import TabbedNavigation from './components/TabbedNavigation.vue'
import Greetings from './componentTabs/HomeGreeting.vue'
import ButtonComponentTab from './componentTabs/ButtonComponent.vue'
import LineComponentTab from './componentTabs/LineComponent.vue'
import SwitchComponentTab from './componentTabs/SwitchComponent.vue'
import InputFieldComponentTab from './componentTabs/InputFieldComponent.vue'
import TextAreaComponentTab from './componentTabs/TextAreaComponent.vue'
import AvatarComponentTab from './componentTabs/AvatarComponent.vue'
import HoverComponentTab from './componentTabs/HoverComponent.vue'
import ExpansionPanelComponentTab from './componentTabs/ExpansionPanelComponent.vue'
import ComboBoxComponentTab from './componentTabs/ComboBoxComponent.vue'
import ImageComponentTab from './componentTabs/ImageComponent.vue'
import AppBarComponentTab from './componentTabs/AppBarComponent.vue'
import BreadCrumbComponentTab from './componentTabs/BreadCrumbComponent.vue'
import CheckboxComponentTab from './componentTabs/CheckboxComponent.vue'
import RadioButtonComponentTab from './componentTabs/RadioButtonComponent.vue'
import RadioButtonGroupComponentTab from './componentTabs/RadioButtonGroupComponent.vue'
import CardComponentTab from './componentTabs/CardComponent.vue'
import TabContainerComponentTab from './componentTabs/TabContainerComponent.vue'
import Footers from './components/Footers.vue'

export default{
  name: 'App',
  components: {
    Tabs,
    TabbedNavigation,
    Greetings,
    ButtonComponentTab,
    LineComponentTab,
    SwitchComponentTab,
    InputFieldComponentTab,
    TextAreaComponentTab,
    AvatarComponentTab,
    HoverComponentTab,
    ExpansionPanelComponentTab,
    ComboBoxComponentTab,
    ImageComponentTab,
    AppBarComponentTab,
    BreadCrumbComponentTab,
    CheckboxComponentTab,
    RadioButtonComponentTab,
    RadioButtonGroupComponentTab,
    CardComponentTab,
    TabContainerComponentTab,
    Footers
  },
}
</script>

<style scoped>

</style>
