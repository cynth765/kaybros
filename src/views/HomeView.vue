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