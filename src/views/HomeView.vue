<script setup>

import ContactUs from '../components/ContactUs.vue';
import Services from '../components/Services.vue';
import Testimonials from '../components/Testimonials.vue';
import Patners from '../components/Patners.vue';
import Map from '../components/Map.vue';



</script>

<template>
  <main class="mt-72 md:mt-0   ">

    <section class=" container mx-auto">
      <div class=" mt-12 flex flex-col-reverse items-center gap-11  md:flex-row ">
      
        <div class="sm:w-1/2 px-11 md:px-0">
         
          <h2 class="text-2xl md:text-3xl  font-semibold  lg:text-4xl text-center max-w-md lg:text-left mb-6">
            KAYBROS GLOBAL CONSULTING LTD
          </h2>
          <p class=" text-lg text-center lg:text-left max-w-md mb-6">
            Kaybros Global consulting ltd mission is to help you grow your company, by getting you to think about future opportunities
          </p>
        
        </div>
        <div class="sm:w-1/2 flex justify-center flex-1 mb-10 md:mb-16 lg:mb-0 z-10">
          <img class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full" src="../components/images/hero-bg.png" alt="" />
        </div>
        <!-- <div class="sm:w-1/2">
          <img src="../components/images/hero-bg.png" alt="" srcset="">

        </div> -->

      </div>
    </section>

  
  
   

    <!-- Services -->
    <section>
      <Services />
    </section>

    <!-- Pattners -->
    <Patners />
    <!-- Map -->
    <Map />




    <!-- About Us -->

  

    <!-- Testimonial -->
    <section class=" ">

      <Testimonials />
        
    </section>



      <!-- Contact Us -->


     <section class=" bg-lime-600">
      <ContactUs/>

     </section>
     
      




  </main>
</template>
