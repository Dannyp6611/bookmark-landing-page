<template>
  <section class="py-20 mt-20 lg:mt-50">
      <!-- Heading -->
      <div class="sm:w-3/4 lg:w-5/12 mx-auto px-2">
        <h2 class="text-3xl text-center text-very-dark-blue font-medium">Features</h2>
        <p class="text-center text-grayish-blue mt-4">
            Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks sync between your devices so you can access them on the go.
        </p>
      </div>
        <ul class="flex flex-col lg:flex-row lg:w-6/12 sm:w-4/5 mt-10 mx-auto lg:border-b-1">
            <li @click="current = 'bookmarking'"
                class="text-sm text-grayish-blue py-4 lg:pb-6 text-center w-2/4 mx-auto border-b-2 lg:flex-1 border-b-white hover:text-soft-red cursor-pointer"
                :class="{ active: current === 'bookmarking' }">Simple Bookmarking</li>
            <li @click="current = 'searching'"
                class="text-sm text-grayish-blue py-4 lg:pb-6 text-center w-2/4 mx-auto border-b-2 lg:flex-1 border-b-white hover:text-soft-red cursor-pointer"
                :class="{ active: current === 'searching' }">Speedy Searching</li>
            <li @click="current = 'sharing'"
                class="text-sm text-grayish-blue py-4 lg:pb-6 text-center w-2/4 mx-auto border-b-2 lg:flex-1 border-b-white hover:text-soft-red cursor-pointer"
                :class="{ active: current === 'sharing' }">Easy Sharing</li>
        </ul>
        <!-- Features -->
        <div v-for="(feature, index) in features" :key="index" class="relative mt-10 lg:mt-24">
            <div v-if="feature.currentFeature === current">
                <div class="container flex flex-col lg:flex-row items-center justify-center gap-x-24">
                <!-- image -->
                <div class="flex flex-1 justify-center z-10 mb-10">
                    <img class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full" 
                        :src="require(`../assets/images/${feature.image}`)" alt="">
                </div>
                <!-- Content -->
                <div class="flex flex-1 flex-col items-center lg:items-start">
                    <h2 class=" text-very-dark-blue text-2xl md:text-4xl lg:text-4xl text-center lg:text-left mb-6">
                        {{ feature.title }}
                    </h2>
                    <p class="text-grayish-blue text-lg text-center lg:text-left my-2 sm:w-3/4 lg:w-full">
                       {{ feature.content }}
                    </p>
                    <button type="button" class="btn btn-dark hover:bg-transparent border-2 hover:text-soft-blue hover:border-soft-blue">
                        More Info
                    </button>
                </div>
            </div>
            <!-- Rounded Rectangle -->
            <div class="hidden lg:block bg-soft-blue overflow-hidden rounded-r-full w-2/4 h-80 absolute -bottom-24 -left-36"></div>
            </div>
        </div>

  </section>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
    setup() {
        const current = ref("bookmarking")
        
        const features = [
                { 
                    title: "Bookmark in one click", 
                    image: "illustration-features-tab-1.svg",
                    content: "Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.",
                    currentFeature: "bookmarking"
                },
                {
                    title: "Intelligent search",
                    image: "illustration-features-tab-2.svg",
                    content: "Our powerful search feature will help you find saved sites in no time at all. No need to trawl through all of your bookmarks.",
                    currentFeature: "searching"
                },
                {
                    title: "Share your bookmarks",
                    image: "illustration-features-tab-3.svg",
                    content: "Easily share your bookmarks and collections with others. Create a shareable link that you can send at the click of a button.",
                    currentFeature: "sharing"
                }
             ]

        return { current, features }
    }
}
</script>

<style>

</style>