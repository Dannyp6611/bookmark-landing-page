<template>
  <div class="w-full h-full font-Poppins overflow-hidden">
    <Header />
    <Hero />
    <Features />
    <Download />
    <FAQ />
    <ContactUs />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue"
import Hero from "@/components/Hero.vue"
import Features from "@/components/Features.vue"
import Download from "@/components/Download.vue"
import FAQ from "@/components/Faq.vue"
import ContactUs from "@/components/ContactUs.vue"
import Footer from "@/components/Footer.vue"

export default {
  name: 'Home',
  components: { Header, Hero, Features, Download, FAQ, ContactUs, Footer }
}
</script>
