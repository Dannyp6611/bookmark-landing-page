<template>
  <section class="relative">
      <div class="container flex flex-col-reverse lg:flex-row items-center gap-12 mt-14 lg:mt-28">
          <!-- Content -->
          <div class="flex flex-1 flex-col items-center lg:items-start">
              <h2 class="capitalize text-very-dark-blue text-3xl md:text-4xl lg:text-5xl text-center lg:text-left mb-6">
                  a simple bookmark manager
              </h2>
              <p class="text-grayish-blue text-lg text-center lg:text-left mb-6">
                  A clean and simple interface to organize your favourite websites. Open a new browser tab and see your sites load instantly. Try it for free.
              </p>
              <div class="flex justify-center flex-wrap gap-6">
                  <button type="button" class="btn btn-dark hover:bg-transparent border-2 hover:text-soft-blue hover:border-soft-blue">Get it on Chrome</button>
                  <button type="button" class="btn btn-light hover:bg-transparent border-2 hover:text-very-dark-blue hover:border-very-dark-blue">Get it on Firefox</button>
              </div>
          </div>
          <!-- Image -->
          <div class="flex justify-center flex-1 mb-10 md:mb-16 lg:mb-0 z-10">
              <img class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full" src="../assets/images/illustration-hero.svg" alt="">
          </div>
      </div>
      <!-- Rounded Rectangle -->
      <div class="hidden md:block bg-soft-blue overflow-hidden rounded-l-full w-2/4 h-80 absolute top-32 right-0 lg:-bottom-28 lg:-right-36"></div>
  </section>
</template>

<script>
export default {

}
</script>

<style>

</style>