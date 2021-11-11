<template>
  <section class="bg-soft-blue text-white py-20">
      <div class="container">
          <div class="sm:w-3/4 lg:w-2/4 mx-auto">
            <p class="tracking-widest font-light text-center mb-8 uppercase text-xs">35,000+ already joined</p>
            <h2 class="text-3xl text-center">Stay up-to-date with what we're doing</h2>
            <div class="flex flex-col sm:flex-row gap-6 mt-8">
                <form @submit.prevent="validateEmail" class="flex flex-1  bg-white rounded-md px-2 justify-between items-center text-very-dark-blue">
                    <input class="w-full focus:outline-none px-4 py-3" type="email" placeholder="Enter your email address" required>
                    <img src="../assets/images/icon-error.svg" alt="" :class="{ hidden: !error }">
                </form>
                <button type="button" class="btn-red hover:bg-white hover:text-soft-red border-2 border-soft-blue hover:border-soft-red">Contact Us</button>
            </div>
          </div>
      </div>
  </section>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
    setup() {
        const error = ref(false)

        const validateEmail = () => {
            error.value = true
        }

        return { error, validateEmail }        
    }
}
</script>

<style>

</style>