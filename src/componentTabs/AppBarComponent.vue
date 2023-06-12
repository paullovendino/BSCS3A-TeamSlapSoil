<template>
  <Template>
      <div class="wrapperLeft">
          <div class="wrapperTop">
              <h1>App Bar Component</h1>
          </div>
          <div class="wrapperBottom">
              <AppBar :title="title" :menuItems="menuItems"/>
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
                    <td>
                        <Checkbox label="Items" name="title" @isChecked="menuItemsEnabled"/>
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
import AppBar from '../components/AppBar.vue'

  export default{
   name: 'ImageComponent',
   components: {
    Template,
    Checkbox,
    AppBar,
},
   data (){
       return{
          title: '',
          menuItems: [
            {label: "", url: "#"},
            {label: "", url: "#"},
            {label: "", url: "#"},
          ]
       }
   },
   methods: {
    titleEnabled(event){
      if(event){
        this.title='Sample Title'
      }else{
        this.title = ''
      }
    },
    menuItemsEnabled(event){
      if(event){
        this.menuItems = [
            {label: "Item 1", url: "#"},
            {label: "Item 2", url: "#"},
            {label: "Item 3", url: "#"},
        ]
      }else{
        this.menuItems =  [
            {label: "", url: "#"},
            {label: "", url: "#"},
            {label: "", url: "#"},
          ]
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
  padding: 10px;
}

.wrapperTop h1{
  color: #7F5539;
}
</style>
