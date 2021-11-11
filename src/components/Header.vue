<template>
  <header>
      <nav class="container flex items-center py-4 mt-4 sm:mt-8">
        <div class="py-1">
            <img src="../assets/images/logo-bookmark.svg" alt="">
        </div>
        <ul class="hidden sm:flex flex-1 justify-end items-center gap-12 text-very-dark-blue uppercase text-xs tracking-wider">
            <li class="hover:text-soft-red cursor-pointer">features</li>
            <li class="hover:text-soft-red cursor-pointer">pricing</li>
            <li class="hover:text-soft-red cursor-pointer">contact</li>
            <button type="button" class="btn-red uppercase tracking-wider border-2 border-white hover:bg-white hover:text-soft-red hover:border-soft-red">login</button>
        </ul>
        <div class="flex sm:hidden flex-1 justify-end items-center cursor-pointer">
            <i class="text-xl fas fa-bars"></i>
        </div>
      </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style>

</style>