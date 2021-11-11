<template>
  <section class="py-14">
        <!-- Heading -->
        <div class="sm:w-3/4 lg:w-5/12 mx-auto px-2">
            <h2 class="text-3xl text-center text-very-dark-blue font-medium">Download the extension</h2>
            <p class="text-center text-grayish-blue mt-4">
               We've got more browsers in the pipeline. Please do let us know if you've got a favourite you'd like us to prioritize.
            </p>
        </div>
        <!-- Cards -->
        <div class="container grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-16 max-w-screen-lg mt-16">
            <div v-for="(card, index) in cards" :key="index">
                <div class="flex flex-col rounded-md shadow-md" :class="card.margin">
                     <div class="p-6 flex flex-col items-center">
                        <img :src="require(`../assets/images/${card.icon}`)" alt="">
                        <h3 class="mt-5 mb-2 text-very-dark-blue text-lg">{{ card.title }}</h3>
                        <p class="mb-2 text-grayish-blue font-light">{{ card.version }}</p>
                    </div>
                    <hr class="border-b border-cool-gray-100 border-dashed" />
                    <div class="flex p-6">
                        <button type="button" class="flex-1 btn btn-dark hover:bg-transparent border-2 hover:text-soft-blue hover:border-soft-blue">
                        Add & Install Extension
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    setup() {
        const cards = [
            {
                title: "Add to Chrome",
                version: "Minimum version 62",
                icon: "logo-chrome.svg",
                margin: "lg:mb-16"
            },
            {
                title: "Add to Firefox",
                version: "Minimum version 55",
                icon: "logo-firefox.svg",
                margin: "lg:my-8"
            },
            {
                title: "Add to Opera",
                version: "Minimum version 46",
                icon: "logo-opera.svg",
                margin: "lg:mt-16"
            }
        ]

        return { cards }
    }
}
</script>

<style>

</style>