<template>
  <Template>
    <div class="wrapperLeft">
      <div class="wrapperTop">
        <h1>Button Component</h1>
      </div>
      <div class="wrapperBottom">
        <BtnSoil :text="BtnText" :type="BtnTypeSelected" :size="BtnSizeSelected" :disabled="BtnDisable"/>
      </div>
    </div>

    <div class="wrapperRight">
      <h2>Attributes</h2>
      <div class="attributes">
        <table>
          <tr>
            <td>
              <Checkbox label="Text" name="text" @isChecked="BtnTextEnabled"/>
            </td>
            <td>
              <Checkbox label="Disabled" name="text" @isChecked="BtnDisabled"/>
            </td>
          </tr>
        </table>
      </div>
      <ExpansionPanel title="Types">
        <table class="expanTable">
          <tr>
            <td><RadioButton label="Default" name="BtnType" value="default" @valueChanged="BtnTypeChanged"/></td>
            <td><RadioButton label="Outline" name="BtnType" value="outlined" @valueChanged="BtnTypeChanged"/></td>
            <td><RadioButton label="Text"  name="BtnType" value="text" @valueChanged="BtnTypeChanged"/></td>
            <td><RadioButton label="Tonal"  name="BtnType" value="tonal" @valueChanged="BtnTypeChanged"/></td>
            <td><RadioButton label="Plain"  name="BtnType" value="plain" @valueChanged="BtnTypeChanged"/></td>
          </tr>
        </table>
      </ExpansionPanel>

      <ExpansionPanel title="Size">
        <table class="expandTable">
          <tr>
            <td><RadioButton label="xx-small" name="BtnSize" value="xx-small" @valueChanged="BtnSizeChanged"/></td>
            <td><RadioButton label="x-small" name="BtnSize" value="x-small" @valueChanged="BtnSizeChanged"/></td>
            <td><RadioButton label="small" name="BtnSize" value="small" @valueChanged="BtnSizeChanged"/></td>
            <td><RadioButton label="medium" name="BtnSize" value="medium" @valueChanged="BtnSizeChanged"/></td>
          </tr>
          <tr>
            <td><RadioButton label="large" name="BtnSize" value="large" @valueChanged="BtnSizeChanged"/></td>
            <td><RadioButton label="x-large" name="BtnSize" value="x-large" @valueChanged="BtnSizeChanged"/></td>
            <td><RadioButton label="xx-large" name="BtnSize" value="xx-large" @valueChanged="BtnSizeChanged"/></td>
          </tr>
        </table>
      </ExpansionPanel>
    </div> 
  </Template>
</template>

<script>
import Template from '/src/components/Content-Template.vue'
import ExpansionPanel from '/src/components/ExpansionPanel.vue'
import Checkbox from '/src/components/Checkbox.vue'
import BtnSoil from '/src/components/BtnSoil.vue'
import RadioButton from '/src/components/RadioButton.vue'

    export default{
     name: 'ButtonComponent',
     components: {
         ExpansionPanel,
         BtnSoil,
         Template,
         Checkbox,
         RadioButton
     },
     data (){
         return{
         BtnTypeSelected: 'default',
         BtnSizeSelected: 'small',
         BtnText: '',
         BtnDisable: false,
         }
     },
     methods: {
         BtnTypeChanged(event){
         this.BtnTypeSelected = event
         },
         BtnSizeChanged(event){
         this.BtnSizeSelected = event
         },
         BtnTextEnabled(event){
         if(event){
             this.BtnText = "Button"
         }else{
             this.BtnText = ''
         }
         },
         BtnDisabled(event){
         if(event){
             this.BtnDisable = true
         }else{
             this.BtnDisable = false
         }
         }
     }
    }
</script>

<style scoped>
.wrapperLeft{
    width: 50%;
    height: 100%;
    padding: 20px;
    padding-right: 10px;
  }

  .wrapperRight{
    padding: 40px;
    width: 50%;
    height: 100%;
    color: #7F5539;
  }

  .attributes{
    width: 100%;
    min-height: 50px;
    background: #e7c2a4;
    border: 2px solid #7F5539;
    border-radius: 20px;
    margin: 10px 0 15px 0;
    min-height: 15%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .expanTable{
    width: 100%;
  }

  table{
    width: 80%;
  }

  .wrapperTop{
    width: 100%;
    height: 10%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .wrapperBottom{
    width: 100%;
    height: 90%;
    border: 2px solid #7F5539;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 30px;
  }

  .wrapperTop h1{
    color: #7F5539;
  }
</style>
