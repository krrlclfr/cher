<script setup>
import Navbar from '@/views/Navbar.vue'
import HeroSection from '@/views/HeroSection.vue'
import About from '@/views/About.vue'
import Skills from '@/views/Skills.vue'
import Project from '@/views/Project.vue'
import Footer from '@/views/Footer.vue'
import Qualification from '@/views/Qualification.vue'
import Contact from '@/views/Contact.vue'
import ArrowUp from '@/components/ArrowUp.vue'
</script>

<template>
  <main> 
    <ArrowUp />
    <Navbar />
    <HeroSection id="Home"/>
    <About id="About"/>
    <Qualification id="Qualification"/>
    <Skills id="Skills"/>
    <Project id="Project"/>
    <Contact id="Contact"/>
    <Footer />
  </main>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');
@font-face {
  font-family: valorant-font;
  src: url('./assets/valorant/Valorant Font.ttf')
}
.text-header {
    font-family: valorant-font;
}
.text-title {
    font-family: "Bebas Neue", sans-serif;
    font-weight: 400;
    font-style: normal;
}
.text-secondary{
  color: #ff4654;
}
.skills-icon {
  font-size: 2.5rem;
  color: #ff4654;
}
.social-media-icon {
  font-size: 1.5rem;
}
</style>
