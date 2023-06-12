<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Avatar Component</h1>
            </div>
            <div class="wrapperBottom">
                <Avatar :imageUrl="imageUrl" :alt="alt" :size="sizeSelected"/>
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <Checkbox label="Image" name="Image" @isChecked="imageEnabled"/>
                    </td>
                    <td>
                        <Checkbox label="Alt" name="alt" @isChecked="altEnabled"/>
                    </td>
                </tr>
                </table>
            </div>
            <ExpansionPanel title="Size">
        <table class="expandTable">
          <tr>
            <td><RadioButton label="xx-small" name="size" value="xx-small" @valueChanged="SizeChanged"/></td>
            <td><RadioButton label="x-small" name="size" value="x-small" @valueChanged="SizeChanged"/></td>
            <td><RadioButton label="small" name="size" value="small" @valueChanged="SizeChanged" checked="true"/></td>
            <td><RadioButton label="medium" name="size" value="medium" @valueChanged="SizeChanged"/></td>
          </tr>
          <tr>
            <td><RadioButton label="large" name="size" value="large" @valueChanged="SizeChanged"/></td>
            <td><RadioButton label="x-large" name="size" value="x-large" @valueChanged="SizeChanged"/></td>
            <td><RadioButton label="xx-large" name="size" value="xx-large" @valueChanged="SizeChanged"/></td>
          </tr>
        </table>
      </ExpansionPanel>
            
        </div> 
    </Template>
</template>

<script>
import Avatar from '/src/components/Avatar.vue'
import Template from '/src/components/Content-Template.vue'
import RadioButton from '/src/components/RadioButton.vue'
import ExpansionPanel from '/src/components/ExpansionPanel.vue'
import Checkbox from '/src/components/Checkbox.vue'

    export default{
     name: 'SwitchComponent',
     components: {
         Avatar,
         Template,
         RadioButton,
         ExpansionPanel,
         Checkbox
     },
     data (){
         return{
            sizeSelected: '',
            imageUrl: '',
            alt: ''
         }
     },
        methods: {
            SizeChanged(event){
                this.sizeSelected = event
            },
            altEnabled(event){
                if(event){
                    this.alt = 'Image'
                }else{
                    this.alt = ''
                }
            },
            imageEnabled(event){
                if(event){
                    this.imageUrl = '/src/assets/img/favicon.ico'
                }else{
                    this.imageUrl = ''
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
