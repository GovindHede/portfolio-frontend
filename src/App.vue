<!-- 

<template>
  <div class="bg-[#111827] min-h-screen"> 
    <Navbar />
    <Hero />
    <About />
    <Skills />
    <Projects />
    <ContactInfo />
     <Footer />
     
  </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';
import Skills from './components/Skills.vue';
import BackToTop from './components/BackToTop.vue';
import LoadingSpinner from './components/LoadingSpinner.vue';

const Navbar = defineAsyncComponent(() => import('@/components/Navbar.vue'));
const Hero = defineAsyncComponent(() => import('@/components/Hero.vue'));
const About = defineAsyncComponent(() =>import('@/components/About.vue'));
const skills = defineAsyncComponent(() =>import('@/components/Skills.vue'));
const Projects = defineAsyncComponent(() =>import('@/components/Projects.vue'));
const ContactInfo = defineAsyncComponent(() =>import('@/components/ContactInfo.vue'));
const Footer = defineAsyncComponent(() =>import('@/components/Footer.vue'));
//const BackToTop = defineAsyncComponent(() =>import('@/components/BackToTop.vue'));
//const LoadingSpinner = defineAsyncComponent(() =>import('@/components/LoadingSpinner.vue'));
import loadingSpinner from './components/loadingSpinner.vue';

</script> -->


<template>
  <div class="bg-[#111827] min-h-screen">
    <!-- Wrap components in Suspense to handle loading -->
     <Suspense>
      <template #default>
        <!-- Wrap all Components inside a single root element -->
         <div>
          <Navbar />
          <Hero />
          <About />
          <skills />
          <Projects />
          <ContactInfo />
          <Footer />
          <BackToTop />
          </div>
    </template>
    <template #fallback>
      <div class="flex justify-center items-center min-h-screen">
          <loadingSpinner />
      </div>
    </template>
  </Suspense>
  </div>
</template>

<script setup>
 import { defineAsyncComponent } from 'vue';
//Import Components Asynchronously
const Navbar = defineAsyncComponent(() => import('@/components/Navbar.vue'));
const Hero = defineAsyncComponent(() => import('@/components/Hero.vue'));
const About = defineAsyncComponent(() =>import('@/components/About.vue'));
const skills = defineAsyncComponent(() =>import('@/components/Skills.vue'));
const Projects = defineAsyncComponent(() =>import('@/components/Projects.vue'));
const ContactInfo = defineAsyncComponent(() =>import('@/components/ContactInfo.vue'));
const Footer = defineAsyncComponent(() =>import('@/components/Footer.vue'));
const BackToTop = defineAsyncComponent(() =>import('@/components/BackToTop.vue'));

import loadingSpinner from './components/loadingSpinner.vue';
</script>
<style>

*{
  scrollbar-width: thin;
  scrollbar-color: #111827 #f1f1f1;
}
</style>
