<template>
    <nav>
      <div class="flext  items-center cursor-pointer mr-96">
                <img class="w-16" src="./images/flogo.png" alt="" srcset=""/>
            </div>
      <div class="menu-item"><router-link to="/">Home</router-link></div>
      <div class="menu-item"><router-link to="/about">About Us</router-link></div>
      <Dropdown title="Services" :items="services" />
      <div class="menu-item"><router-link to="/industries">KGC Foundation</router-link></div>
      <div class="menu-item"><router-link to="/contact">Countact Us</router-link></div>
      
    </nav>
  </template>
  
  <script>
 import Dropdown from './dropdown.vue'
  export default {
    name: 'Navigation',
    components: {
      Dropdown
    },
    data () {
      return {
        services: [
          {
            title: 'Tax Compliance ',
            link: '/tax'
          },
          {
            title: 'Human Resource ',
            link:'/resource'
          },
          {
            title: 'Business',
            link: '/business'
          }
        ]
      }
    }
  }
  </script>
  
  <style>
  nav {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: grey;
  }
  nav .menu-item {
    color: white;
    padding: 10px 20px;
    position: relative;
    text-align: center;
    border-bottom: 3px solid transparent;
    display: flex;
    transition: 0.4s;
  }
  nav .menu-item.active,
  nav .menu-item:hover {
    background-color: #046473;
    border-bottom-color: #046473;
  }
  nav .menu-item a {
    color: inherit;
    text-decoration: none;
  }
  </style>