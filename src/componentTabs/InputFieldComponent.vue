<template>
    <Template>
      <div class="wrapperLeft">
        <div class="wrapperTop">
          <h1>Input Field Component</h1>
        </div>
        <div class="wrapperBottom">
          <InputField :type="typeSelected" :placeholder="placeholder" :readonly="readOnly" :disabled="disabled" />
        </div>
      </div>
  
      <div class="wrapperRight">
        <h2>Attributes</h2>
        <div class="attributes">
          <table>
            <tr>
              <td>
                <Checkbox label="Placeholder" name="placeholder" @isChecked="placeholderEnabled"/>
              </td>
              <td>
                <Checkbox label="Disabled" name="disabled" @isChecked="isDisabled"/>
              </td>
              <td>
                <Checkbox label="Read-Only" name="read-only" @isChecked="readOnlyEnabled"/>
              </td>
            </tr>
          </table>
        </div>
  
        <ExpansionPanel title="Types">
          <table class="expandTable">
            <tr>
              <td><RadioButton label="Default" name="type" value="default" @valueChanged="TypeChanged" checked="true"/></td>
              <td><RadioButton label="Dark" name="type" value="dark" @valueChanged="TypeChanged"/></td>
              <td><RadioButton label="Underlined Light" name="type" value="underlined-light" @valueChanged="TypeChanged"/></td>
            </tr>
            <tr>
              <td><RadioButton label="Underlined Dark" name="type" value="underlined-dark" @valueChanged="TypeChanged"/></td>
              <td><RadioButton label="Outlined Light" name="type" value="outlined-light" @valueChanged="TypeChanged"/></td>
              <td><RadioButton label="Outlined Dark" name="type" value="outlined-dark" @valueChanged="TypeChanged"/></td>
            </tr>
            <tr>
              <td><RadioButton label="Solo" name="type" value="solo" @valueChanged="TypeChanged"/></td>
              <td><RadioButton label="Solo Filled" name="type" value="solo-filled" @valueChanged="TypeChanged"/></td>
              <td><RadioButton label="Solo Inverted" name="type" value="solo-inverted" @valueChanged="TypeChanged"/></td>
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
  import RadioButton from '/src/components/RadioButton.vue'
  import InputField from '/src/components/InputField.vue'
  
      export default{
       name: 'InputFieldComponent',
       components: {
           ExpansionPanel,
           Template,
           Checkbox,
           RadioButton,
           InputField
       },
       data (){
           return{
           typeSelected: '',
           placeholder: '',
           readOnly: false,
           disabled: false,
           }
       },
       methods: {
           TypeChanged(event){
            this.typeSelected = event
           },
           placeholderEnabled(event){
            if(event){
                this.placeholder = 'Type your text here'
            }else{
                this.placeholder = ''
            }
           },
           readOnlyEnabled(event){
            this.readOnly = event
           },
           isDisabled(event){
                this.disabled = event
           },
           
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
