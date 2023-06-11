<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Radiobutton Component</h1>
            </div>
            <div class="wrapperBottom">
                <table>
                    <tr>
                        <RadioButton :label="label" name="sample" :checked="checked" :disabled="disabled"/>
                    </tr>
                    <tr>
                        <RadioButton :label="label" name="sample" :disabled="disabled"/>
                    </tr>
                </table>
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <Checkbox label="Label" name="label" @isChecked="labelEnabled"/>
                    </td>
                    <td>
                        <Checkbox label="Checked" name="checked" @isChecked="checkChange"/>
                    </td>
                    <td>
                        <Checkbox label="Disabled" name="disabled" @isChecked="disabledChange"/>
                    </td>
                </tr>
                </table>
            </div>
        </div> 
    </Template>
</template>

<script>
import Template from '/src/components/Content-Template.vue'
import Checkbox from '/src/components/Checkbox.vue'
import RadioButton from '../components/RadioButton.vue'

    export default{
     name: 'CheckboxComponent',
     components: {
        Template,
        Checkbox,
        RadioButton
    },
     data (){
         return{
            disabled: false,
            checked: false,
            label: ' ',
         }
     },
     methods: {
         checkChange(event){
            this.checked = event
            console.log(event)
         },
         disabledChange(event){
            this.disabled = event
         },
         labelEnabled(event){
            if(event){
                this.label = "Radiobutton"
            }else{
                this.label = ''
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