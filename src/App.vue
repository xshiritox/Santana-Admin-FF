<script setup lang="ts">
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import HowItWorks from './components/HowItWorks.vue'
import Testimonials from './components/Testimonials.vue'
import Contact from './components/Contact.vue'
import Policies from './components/Policies.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="app">
    <Navbar />
    <Hero />
    <About />
    <HowItWorks />
    <Testimonials />
    <Contact />
    <Policies />
    <Footer />
  </div>
</template>

<style scoped>
.app {
  width: 100%;
  overflow-x: hidden;
}
</style>
