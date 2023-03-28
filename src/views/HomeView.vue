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
    <section class="mt-28">
    <Slider />
  </section>
  



    
  
<!-- 
    <section class="mt-20">
      <Services />
    </section> -->

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
  data() {
    return {
      images: [
        'https://via.placeholder.com/500x300?text=Slide+1',
        'https://via.placeholder.com/500x300?text=Slide+2',
        'https://via.placeholder.com/500x300?text=Slide+3',
      ],
      currentIndex: 0,
    };
  },
  mounted() {
    setInterval(() => {
      this.currentIndex =
        (this.currentIndex + 1) % this.images.length;
    }, 3000);
  },
};  <script>
      let slideIndex = 0;
      let timeoutId = null;
      const slides = document.getElementsByClassName("mySlides");
      const dots = document.getElementsByClassName("dot");
      
      showSlides();
      function currentSlide(index) {
           slideIndex = index;
           showSlides();
      }
     function plusSlides(step) {
        
        if(step < 0) {
            slideIndex -= 2;
            
            if(slideIndex < 0) {
              slideIndex = slides.length - 1;
            }
        }
        
        showSlides();
     }
      function showSlides() {
        for(let i = 0; i < slides.length; i++) {
          slides[i].style.display = "none";
          dots[i].classList.remove('active');
        }
        slideIndex++;
        if(slideIndex > slides.length) {
          slideIndex = 1
        }
        slides[slideIndex - 1].style.display = "block";
        dots[slideIndex - 1].classList.add('active');
         if(timeoutId) {
            clearTimeout(timeoutId);
         }
        timeoutId = setTimeout(showSlides, 5000); // Change image every 5 seconds
      }
    



</script> -->
