<template>
    
        <div class="  bg-gray-100   py-3.5  px-6 shadow  md:flex  justify-between items-center md:w-auto w-full">
            <!-- Logo -->
            <div class="flext  items-center cursor-pointer">
                <img class="" src="./images/logo.svg" alt="" srcset=""/>
            </div>

            <span @click="MenuOPen()" class="absolute right-6 top-1.5 cursor-pointer text-4xl md:hidden">
                <i :class="[open ? 'bi bi-x' : 'bi bi-filter-left']"></i>

            </span>
            <!-- Menu Items -->
            <ul class="  md:flex md:items-center  md:px-0 px-6 md:pb-0 pb-10 md:static absolute
             md:w-auto w-full top-14 duration-100 ease-in "
            :class="[ open? 'left-0': 'left-[-100%]']"  >
                <li class="md:mx-4 md:my-0 my-6 " v-for="link in Links">
                    <a :href="link.link" class="text-xl">{{ link.name }}</a>
                
                </li>
                 <Button />
            
            </ul>
        
        </div>
       
</template>

<script setup>
import { ref } from 'vue';

import Button from './Button.vue'



const open = ref(false);
let Links = [
    {name: "Home", link: "/"},
    {name: "About", link: "/about"},
    {name: "Contact", link: "/contact"},
    {name: "Services", link: "/services"}
]
function MenuOPen() {
    open.value = !open.value;
    
}

</script>

<style lang="scss" scoped>

</style>