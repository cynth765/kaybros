<template>
    <nav>
      <div class="flext  items-center cursor-pointer mr-96">
                <img class="rounded-full w-10" src="https://th.bing.com/th/id/OIP.fmafBBwHnDOnRcKJdCwGgQHaHa?pid=ImgDet&w=183&h=183&c=7" alt="" srcset=""/>
            </div>
      <div class="menu-item"><router-link to="/">Home</router-link></div>
      <div class="menu-item"><router-link to="/about">About Us</router-link></div>
      <Dropdown title="Services" :items="services" />
      <div class="menu-item"><router-link to="/industries">KGC Foundation</router-link></div>
      <div class="menu-item"><router-link to="/contact">Countact Us</router-link></div>
      
    </nav>
  </template>
  
  <script>
 import Dropdown from './Dropdown.vue'
  export default {
    name: 'Navigation',
    components: {
      Dropdown
    },
    data () {
      return {
        services: [
          {
            title: 'Audit and Assurrance ',
            link: '/tax'
          },
          {
            title: 'Human Resource Management ',
            link:'/resource'
          },
          {
            title: 'Business Valuation',
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
    background-color: black;
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
  @media only screen and (max-width: 1024px) {
  nav {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    justify-content: center;
  }
  nav .menu-item {
    width: 100%;
    padding: 10px;
    border-bottom: 1px solid white;
    text-align: center;
    transition: 0.4s;
  }
  nav .menu-item.active,
  nav .menu-item:hover {
    background-color: #046473;
    border-bottom-color: #046473;
  }
  nav .menu-item a {
    color: white;
    text-decoration: none;
  }
  .flext {
    margin-right: 0;
  }
}


  </style>