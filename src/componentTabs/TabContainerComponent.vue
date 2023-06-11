<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Tab Container</h1>
            </div>
            <div class="wrapperBottom">
                <TabContainer :Container_Title="title">
                    <Tabs title="Item 1">
                        Item 1
                    </Tabs>
                    <Tabs title="Item 2">
                        Item 2
                    </Tabs>
                    <Tabs title="Item 3">
                        Item 3
                    </Tabs>
                </TabContainer>
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <Checkbox label="Title" name="title" @isChecked="titleEnabled"/>
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
import Tabs from '/src/components/navTabs.vue'
import TabContainer from '/src/components/TabContainer.vue'

    export default{
     name: 'TabContainerComponent',
     components: {
        Template,
        Checkbox,
        Tabs,
        TabContainer,
     },
     data (){
         return{
            title: '',
         }
     },
     methods: {
        titleEnabled(event){
            if(event){
                this.title="Sample"
            }else{
                this.title=' '
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