<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Switch Component</h1>
            </div>
            <div class="wrapperBottom">
                <Switch :checked="SwitchOn" :disabled="Disabled" :type="typeSelected" />
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <Checkbox label="On" name="switchLabel" @isChecked="SwitchChanged"/>
                    </td>
                    <td>
                        <Checkbox label="Disabled" name="text" @isChecked="isDisabled"/>
                    </td>
                </tr>
                </table>
            </div>

            <ExpansionPanel title="Types">
                <table class="expandTable">
                <tr>
                    <td><RadioButton label="Rectangular" name="switchType" value="rectangular" @valueChanged="TypeChanged" checked="true"/></td>
                    <td><RadioButton label="Round" name="switchType" value="round" @valueChanged="TypeChanged"/></td>
                </tr>
                </table>
            </ExpansionPanel>
            
        </div> 
    </Template>
</template>

<script>
import Template from '/src/components/Content-Template.vue'
import RadioButton from '/src/components/RadioButton.vue'
import Switch from '/src/components/Switch.vue'
import ExpansionPanel from '/src/components/ExpansionPanel.vue'
import Checkbox from '/src/components/Checkbox.vue'

    export default{
     name: 'SwitchComponent',
     components: {
         Switch,
         Template,
         RadioButton,
         ExpansionPanel,
         Checkbox
     },
     data (){
         return{
            SwitchOn: false,
            Disabled: false,
            typeSelected: ''
         }
     },
        methods: {
            SwitchChanged(event){
                this.SwitchOn = event
            },
            isDisabled(event){
                this.Disabled = event
            },
            TypeChanged(event){
                this.typeSelected = event
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

  .expandTable{
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
