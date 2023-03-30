<template>
  <div class="relative">
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-y-0 left-0 w-full bg-gray-900 bg-opacity-50"></div>
      <div class="h-full w-full flex">
        <div v-for="(image, index) in images" :key="index" :style="{ transform: `translateX(-${index * 100}%)`, backgroundImage: `url(${image})` }" class="h-full w-full absolute inset-0 bg-cover bg-no-repeat"></div>
      </div>
    </div>
    <div class="relative z-10 max-w-7xl mx-auto py-24 px-4 sm:px-6 lg:px-8">
      <h1 class="text-4xl font-extrabold tracking-tight text-white sm:text-5xl md:text-6xl">
        <span class="block xl:inline">KAYBROS GLOBAL CONSULTING LTD</span>
      </h1>
      <p class="mt-6 text-xl text-white max-w-3xl">
        "Accounting is the backbone of the business financial world." - Richard J. Curwin
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        'https://images.pexels.com/photos/3214958/pexels-photo-3214958.jpeg?auto=compress&cs=tinysrgb&w=600',
        'https://images.pexels.com/photos/1098365/pexels-photo-1098365.jpeg?auto=compress&cs=tinysrgb&w=600',
        'https://images.pexels.com/photos/1819657/pexels-photo-1819657.jpeg?auto=compress&cs=tinysrgb&w=600',
      ]
    }
  },
  mounted() {
    // Preload images
    this.images.forEach((image) => {
      new Image().src = image;
    });
    // Set interval for sliding images
    setInterval(() => {
      this.images.push(this.images.shift());
    }, 5000);
  }
}
</script>

<style scoped>
/* Set background images */
div[h-full] {
  background-image: url('https://images.pexels.com/photos/3214958/pexels-photo-3214958.jpeg?auto=compress&cs=tinysrgb&w=600');
}
div[h-full]:nth-of-type(2) {
  background-image: url('https://images.pexels.com/photos/1098365/pexels-photo-1098365.jpeg?auto=compress&cs=tinysrgb&w=600');
}
div[h-full]:nth-of-type(3) {
  background-image: url('https://images.pexels.com/photos/1819657/pexels-photo-1819657.jpeg?auto=compress&cs=tinysrgb&w=600');
}
</style>
