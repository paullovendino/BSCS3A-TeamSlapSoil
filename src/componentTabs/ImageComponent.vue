<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Image Component</h1>
            </div>
            <div class="wrapperBottom">
                <Image/>
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <Checkbox label="With Text" name="ShowLabel"/>
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
                    <td><RadioButton label="Option 1" name="switchType" value=" " @valueChanged="TypeChanged" checked="true"/></td>
                    <td><RadioButton label="Option 2" name="switchType" value=" " @valueChanged="TypeChanged"/></td>
                </tr>
                </table>
            </ExpansionPanel>
            
        </div> 
    </Template>
</template>

<script>
import Template from '/src/components/Content-Template.vue'
import RadioButton from '/src/components/RadioButton.vue'
import Image from '/src/components/Image.vue'
import ExpansionPanel from '/src/components/ExpansionPanel.vue'
import Checkbox from '/src/components/Checkbox.vue'

    export default{
     name: 'SwitchComponent',
     components: {
         Image,
         Template,
         RadioButton,
         ExpansionPanel,
         Checkbox
     },
     data (){
         return{
            Disabled: false,
            typeSelected: ''
         }
     },
        methods: {

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