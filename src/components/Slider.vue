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
        'https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTR8fGFjY291bnRpbmd8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60',
        'https://images.pexels.com/photos/7063765/pexels-photo-7063765.jpeg?auto=compress&cs=tinysrgb&w=600',
        'https://images.unsplash.com/photo-1554224155-3a58922a22c3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTd8fGFjY291bnRpbmd8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60',
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
  background-image: url('https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTR8fGFjY291bnRpbmd8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60');
}
div[h-full]:nth-of-type(2) {
  background-image: url('https://images.pexels.com/photos/7063765/pexels-photo-7063765.jpeg?auto=compress&cs=tinysrgb&w=600');
}
div[h-full]:nth-of-type(3) {
  background-image: url('https://images.unsplash.com/photo-1554224155-3a58922a22c3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTd8fGFjY291bnRpbmd8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60');
}
</style>
