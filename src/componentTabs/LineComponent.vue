<template>
    <Template>
        <div class="wrapperLeft">
            <div class="wrapperTop">
                <h1>Line Component</h1>
            </div>
            <div class="wrapperBottom">
                <Line :alignment="alignmentSelected"/>
            </div>
        </div>

        <div class="wrapperRight">
            <h2>Attributes</h2>
            <div class="attributes">
                <table>
                <tr>
                    <td>
                        <RadioButton label="Vertical" name="alignment" value="vertical" @valueChanged="alignmentChanged"/>
                    </td>
                    <td>
                        <RadioButton label="Horizontal" name="alignment" value="horizontal" @valueChanged="alignmentChanged"/>
                    </td>
                </tr>
                </table>
            </div>
        </div> 
    </Template>
</template>

<script>
import Template from '/src/components/Content-Template.vue'
import RadioButton from '/src/components/RadioButton.vue'
import Line from '/src/components/Line.vue'

    export default{
     name: 'LineComponent',
     components: {
         Line,
         Template,
         RadioButton
     },
     data (){
         return{
            alignmentSelected: 'default',
         }
     },
     methods: {
         alignmentChanged(event){
            this.alignmentSelected = event
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