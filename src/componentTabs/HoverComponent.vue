<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Hover Component</h1>
            </div>
            <div class="wrapperBottom">
                <Hover :disabled="Disabled" :hovereffect="hoverEffect" :shape="shape">Sample</Hover>
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

            <ExpansionPanel title="Shape">
                <table class="expandTable">
                <tr>
                    <td><RadioButton label="Rectangle" name="shape" value="rectangle" @valueChanged="shapeChanged" checked="true"/></td>
                    <td><RadioButton label="Round" name="shape" value="round" @valueChanged="shapeChanged"/></td>
                </tr>
                </table>
            </ExpansionPanel>

            <ExpansionPanel title="Types">
                <table class="expandTable">
                <tr>
                    <td><RadioButton label="Default" name="hoverEffect" value="default" @valueChanged="HoverChanged" checked="true"/></td>
                    <td><RadioButton label="Underlined" name="hoverEffect" value="underlined" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Text Color" name="hoverEffect" value="text-color" @valueChanged="HoverChanged"/></td>
                </tr>
                <tr>
                    <td><RadioButton label="Zoom In" name="hoverEffect" value="zoom-in" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Zoom Out" name="hoverEffect" value="zoom-out" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Border" name="hoverEffect" value="border" @valueChanged="HoverChanged"/></td>
                </tr>
                <tr>
                    <td><RadioButton label="Right Tilt" name="hoverEffect" value="right-tilt" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Left Tilt" name="hoverEffect" value="left-tilt" @valueChanged="HoverChanged"/></td>
                    <td><RadioButton label="Shadow" name="hoverEffect" value="shadow" @valueChanged="HoverChanged"/></td>
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
            hoverEffect: '',
            shape: '',
         }
     },
        methods: {
            isDisabled(event){
                this.Disabled = event
            },
            HoverChanged(event){
                this.hoverEffect = event
            },
            shapeChanged(event){
                this.shape = event
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
