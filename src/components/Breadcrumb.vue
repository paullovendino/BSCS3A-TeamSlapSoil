<template>
    <nav class="breadcrumb">
      <ul>
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
      items: [],
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
  }
  
  li {
    display: inline-block;
    margin-right: 5px;
  }
  
  a {
    text-decoration: none;
    color: #ffe1a8;
  }
  
  a.active {
    color: #f08080;
    font-weight: bold;
  }
  
  .divider {
    margin: 0 5px;
    color: #ffea00;
  }
  </style>
  
