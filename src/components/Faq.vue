<template>
  <section class="py-20">
      <div class="container">
          <!-- Heading -->
          <div class="sm:w-3/4 lg:w-5/12 mx-auto px-2">
            <h2 class="text-3xl text-center text-very-dark-blue font-medium">FAQ</h2>
            <p class="text-center text-grayish-blue mt-4">
               Here are some of our FAQS. If you have any other questions you'd like answered please feel free to email us.
            </p>
        </div>
        <!-- FAQ ITEMS -->
        <div class="flex flex-col sm:w-3/4 lg:w-5/12 mt-6 mx-auto" v-for="(question, index) in faqItems" :key="index">
            <div class="border-b py-2 cursor-pointer" @click="question.active = !question.active">
                <div class="flex items-center">
                    <span class="flex-1 hover:text-soft-red">{{ question.title }}</span>
                    <i class="fas fa-chevron-down justify-end text-soft-blue" :class="{ 'text-soft-red transform rotate-180': question.active }"></i>
                </div>
                <p v-if="question.active" class="text-grayish-blue py-4">{{ question.description }}</p>
            </div>
        </div>
        <div class="flex py-4 mt-10 justify-center">
            <button type="button" class="btn btn-dark hover:bg-transparent border-2 hover:text-soft-blue hover:border-soft-blue">
                        More Info
            </button>
        </div>
      </div>
  </section>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
    setup() {
        const faqItems = ref([
            {
                title: "What is Bookmark?",
                description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt repellendus asperiores aliquid unde repudiandae voluptate repellat eos, neque, perferendis quasi similique et ea incidunt aperiam atque dicta provident veritatis non debitis, voluptatum ab quod qui minus nemo! Corporis, commodi quae velit quas eligendi iste, doloribus repellendus ipsa asperiores, corrupti alias.",
                active: false
            },
            {
                title: "How can i request a new browser?",
                description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt repellendus asperiores aliquid unde repudiandae voluptate repellat eos, neque, perferendis quasi similique et ea incidunt aperiam atque dicta provident veritatis non debitis, voluptatum ab quod qui minus nemo! Corporis, commodi quae velit quas eligendi iste, doloribus repellendus ipsa asperiores, corrupti alias.",
                active: false
            },
            {
                title: "Is there a mobile app?",
                description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt repellendus asperiores aliquid unde repudiandae voluptate repellat eos, neque, perferendis quasi similique et ea incidunt aperiam atque dicta provident veritatis non debitis, voluptatum ab quod qui minus nemo! Corporis, commodi quae velit quas eligendi iste, doloribus repellendus ipsa asperiores, corrupti alias.",
                active: false
            },
            {
                title: "What about other Chromium browsers?",
                description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt repellendus asperiores aliquid unde repudiandae voluptate repellat eos, neque, perferendis quasi similique et ea incidunt aperiam atque dicta provident veritatis non debitis, voluptatum ab quod qui minus nemo! Corporis, commodi quae velit quas eligendi iste, doloribus repellendus ipsa asperiores, corrupti alias.",
                active: false
            }
        ])
        

        return { faqItems }
    }
}
</script>

<style>

</style>