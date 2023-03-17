<script setup>
import ContactUs from '../components/ContactUs.vue';
import Services from '../components/Services.vue';
import Testimonials from '../components/Testimonials.vue';
import Patners from '../components/Patners.vue';
import Map from '../components/Map.vue';

import Slider from '../components/Slider.vue'
import footer from "../components/footer.vue"
</script>

<template>
  <main class="">
    <!-- <section>
    <Slider />
  </section> -->
  <!-- <section>
  <div class="">
    <transition-group name="fade" tag="div">
      <div v-for="i in [currentIndex]" :key="i" class="imag">
        <img :src="currentImg" />
      </div>
    </transition-group>
    <a class="prev" @click="prev" href="#">&#10094; Previous</a>
    <a class="next" @click="next" href="#">&#10095; Next</a>
  </div>
</section> -->
<!-- <Slider/> -->

    <!-- Services -->
    <div class="bg-cover bg-center h-screen" style="background-image: url('https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg') opacity-10">
  <div class="h-screen flex items-center justify-center">
    <h2 class="text-2xl md:text-3xl  font-semibold  lg:text-4xl text-center max-w-md lg:text-left mb-6 text-white">
      KAYBROS GLOBAL CONSULTING LTD
     </h2>
     <h2 class="text-white text-2xl md:text-3xl "> We Nurture You</h2>
  </div>
  
</div>

    <section class="mt-20">
      <Services />
    </section>

    <!-- Pattners -->
    <!-- <Patners /> -->
    <!-- Map -->
    <section>
    <Map />
  </section>




    <!-- About Us -->

  

    <!-- Testimonial -->
    <section class=" ">

      <!-- <Testimonials /> -->
        
    </section>



      <!-- Contact Us -->


     <section class=" bg-lime-600">
      <footer/>

     </section>
     
      




  </main>
</template>
<style>
.container {
  position: relative;
  text-align: center;
  color: white;
}

/* Bottom left text */
.bottom-left {
  position: absolute;
  bottom: 8px;
  left: 16px;
}

/* Top left text */
.top-left {
  position: absolute;
  top: 8px;
  left: 16px;
}

/* Top right text */
.top-right {
  position: absolute;
  top: 8px;
  right: 16px;
}

/* Bottom right text */
.bottom-right {
  position: absolute;
  bottom: 8px;
  right: 16px;
}

/* Centered text */
.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}


</style>
<!-- <script>
export default {
  name: "Slider",
  data() {
    return {
      images: [
        "https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg",
        "https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg",
        
      ],
      timer: null,
      currentIndex: 0,
      show: true
    };
  },

  mounted: function() {
    this.startSlide();
  },

  methods: {
    startSlide: function() {
      this.timer = setInterval(this.next, 4000);
    },

    next: function() {
      this.currentIndex += 1;
    },
    prev: function() {
      this.currentIndex -= 1;
    }
  },

  computed: {
    currentImg: function() {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
    }
  }
};
</script> -->