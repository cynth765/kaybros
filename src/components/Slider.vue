<template>
  <div class="slideshow-container min-h-screen w-screen">
    <div v-for="(image, index) in images" :key="index" :class="[slideClasses(index)]">
      <div class="relative h-screen">
        <div class="absolute inset-0 bg-cover" :style="{ backgroundImage: `url(${image})` }"></div>
        <div class="absolute bottom-0 left-0 p-4">
          <h2 class="text-4xl font-bold text-white">Slide {{ index + 1 }}</h2>
          <p class="text-xl text-white">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.slideshow-container {
  overflow: hidden;
}
</style>

<script>
export default {
  data() {
    return {
      images: [
        'https://picsum.photos/1200/800?random=1',
        'https://picsum.photos/1200/800?random=2',
        'https://picsum.photos/1200/800?random=3',
      ],
      currentSlide: 0,
    };
  },
  mounted() {
    setInterval(() => {
      this.currentSlide = (this.currentSlide + 1) % this.images.length;
    }, 5000);
  },
  methods: {
    slideClasses(index) {
      const currentIndex = this.currentSlide;
      const lastIndex = this.images.length - 1;
      const position = index - currentIndex;

      return {
        'absolute h-screen w-full transition-transform duration-500': true,
        'transform translate-x-full': position === lastIndex,
        'transform translate-x-0': position === 0,
        'transform -translate-x-full': position === -1,
        'opacity-0': position < -1 || position > 1,
      };
    },
  },
};
</script>

