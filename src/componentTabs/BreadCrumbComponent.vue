<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>BreadCrumb Component</h1>
            </div>
            <div class="wrapperBottom">
                <BreadCrumb :items="items" :type="type"/>
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <Checkbox label="Items" name="items" @isChecked="itemsEnabled"/>
                    </td>
                </tr>
                </table>
            </div>

            <ExpansionPanel title="Types">
                <table class="expandTable">
                <tr>
                    <td><RadioButton label="Default" name="type" value="default" @valueChanged="TypeChanged" checked="true"/></td>
                    <td><RadioButton label="Background" name="type" value="background" @valueChanged="TypeChanged"/></td>
                </tr>
                </table>
            </ExpansionPanel>
            
        </div> 
    </Template>
</template>

<script>
import Template from '/src/components/Content-Template.vue'
import Checkbox from '/src/components/Checkbox.vue'
import BreadCrumb from '/src/components/breadcrumb.vue'
import ExpansionPanel from '/src/components/ExpansionPanel.vue'
import RadioButton from '/src/components/RadioButton.vue'

    export default{
     name: 'SwitchComponent',
     components: {
         BreadCrumb,
         Template,
         Checkbox,
         ExpansionPanel,
         RadioButton
     },
     data (){
         return{
          items: [
            {label: "", url: "#"},
          ],
          type: '',
         }
     },
        methods: {
          itemsEnabled(event){
            if(event){
              this.items = [
                  {label: "Item 1", url: "#"},
                  {label: "Item 2", url: "#"},
                  {label: "Item 3", url: "#"},
              ]
            }else{
              this.items =  [
                  {label: "", url: "#"}
                ]
            }
          },
          TypeChanged(event){
            this.type = event
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
