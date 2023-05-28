<template>
    <div class="app-bar">
      <div class="menu-button" @click="toggleDropdown">
        <div class="menu-icon">
          <div class="line"></div>
          <div class="line"></div>
          <div class="line"></div>
        </div>
      </div>
      <h1 class="title">{{ title }}</h1>
      <ul class="menu" :class="{ 'open': dropdownOpen }">
        <li v-for="(item, index) in menuItems" :key="index">
          <a :href="item.url">{{ item.label }}</a>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'AppBar',
    props: {
      title: {
        type: String,
        required: true
      },
      menuItems: {
        type: Array,
        required: true
      }
    },
    data() {
      return {
        dropdownOpen: false
      };
    },
    methods: {
      toggleDropdown() {
        this.dropdownOpen = !this.dropdownOpen;
      }
    }
  };
  </script>
  
  <style>
  .app-bar {
    display: flex;
    align-items: center;
    background-color: #7F5539;
    padding: 10px;
    position: relative;
    color: white;
    margin-top: 3px;
  }
  
  .menu-button {
    cursor: pointer;
    background: none;
    border: none;
    padding: 0;
    margin-right: 10px;
  }
  
  .menu-icon {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 25px;
    height: 20px;
  }
  
  .line {
    width: 100%;
    height: 2px;
    background-color: #E6CCB2;
  }
  
  .title {
    margin-left: 10px;
  }
  
  .menu {
    display: none;
    list-style: none;
    position: absolute;
    top: calc(100% + 0px);
    left: 0;
    background-color: #E6CCB2;
    padding: 10px;
    margin: 0;
    width: 200px;
  }
  
  .menu.open {
    display: block;
  }
  
  .menu li {
    margin-bottom: 10px;
  }
  
  .menu a {
    text-decoration: none;
    color: #7F5539;
  }
  
  .menu a:hover {
    background-color: #7F5539;
    color: white;
  }
  </style>