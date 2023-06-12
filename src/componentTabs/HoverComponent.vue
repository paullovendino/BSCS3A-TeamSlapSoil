<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Hover Component</h1>
            </div>
            <div class="wrapperBottom">
                <Hover :disabled="Disabled" :type="HoverSelected"/>
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <Checkbox label="Disable" name="text" @isChecked="isDisabled"/>
                    </td>
                </tr>
                </table>
            </div>

            <ExpansionPanel title="Types">
                <table class="expandTable">
                <tr>
                    <td><RadioButton label="Background" name="switchEffect" value="ChangeBackgroundColor" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Underlined" name="switchEffect" value="Underlined" @valueChanged="HoverChanged" checked="true"/></td>
                    <td><RadioButton label="Text Color" name="switchEffect" value="ChangeTextColor" @valueChanged="HoverChanged"/></td>
                </tr>
                <tr>
                    <td><RadioButton label="Zoom In" name="switchEffect" value="ZoomIn" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Zoom Out" name="switchEffect" value="ZoomOut" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Text Zoom" name="switchEffect" value="TextZoom" @valueChanged="HoverChanged"/></td>
                </tr>
                <tr>
                    <td><RadioButton label="Right Tilt" name="switchEffect" value="RightTilt" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Left Tilt" name="switchEffect" value="LeftTilt" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Border" name="switchEffect" value="BorderLine" @valueChanged="HoverChanged"/></td>
                </tr>
                </table>
            </ExpansionPanel>
            
        </div> 
    </Template>
</template>

<script>
import Template from '/src/components/Content-Template.vue'
import RadioButton from '/src/components/RadioButton.vue'
import Hover from '/src/components/Hover.vue'
import ExpansionPanel from '/src/components/ExpansionPanel.vue'
import Checkbox from '/src/components/Checkbox.vue'

    export default{
     name: 'SwitchComponent',
     components: {
         Hover,
         Template,
         RadioButton,
         ExpansionPanel,
         Checkbox
     },
     data (){
         return{
            Disabled: false,
            HoverSelected: ''
         }
     },
        methods: {
            isDisabled(event){
                this.Disabled = event
            },
            HoverChanged(event){
                this.HoverSelected = event
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