<template>
    <nav class="breadcrumb">
      <ul :class="type">
        <li v-for="(item, index) in items" :key="index">
          <a :href="item.url" :class="{ 'active': index === items.length - 1 }">{{ item.label }}</a>
          <span v-if="index !== items.length - 1" class="divider">/</span>
        </li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    props: {
      items: {
        type: Array,
        required: true
      },
      type: String,
    }
  };
  </script>
  
  <style>
  .breadcrumb {
    background-color: none;
    padding: 10px;
  }
  
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    padding: 15px;
  }
  
  li {
    display: inline-block;
    margin-right: 5px;
  }
  
  a {
    text-decoration: none;
    color: #dba981;
  }
  
  a.active {
    color: #7F5539;
    font-weight: bold;
  }
  
  .divider {
    margin: 0 5px;
    color: #593b27;
  }

  .background{
    background: #7F5539;
  }

  .background a{
    color: #af8665;
  }

  .background a.active{
    color: #f6e4d5;
  }

  .background .divider{
    color: #ecb274;
  }
  </style>
  
