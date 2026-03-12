<template>
   <div class="min-h-screen bg-[#0a0f1d]">  
      <Navbar />
      <Hero />
      <Trayectoria/>
      <Expertise />
      <Proyectos/>
      <Footer />

      <ScrollToTop />
  </div> 
</template>

<script setup>
import { ref, onMounted, nextTick } from 'vue';
import Aos from 'aos';
import 'aos/dist/aos.css';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Trayectoria from './components/Trayectoria.vue';
import Expertise from './components/Expertise.vue';
import Proyectos from './components/Proyectos.vue';
import Footer from './components/Footer.vue';
import ScrollToTop from './components/ScrollToTop.vue';

const loading = ref(true);

onMounted(async ()=>{
  await nextTick();

  Aos.init({
    duration:800,
    once:false,
    offset:100,
    easing:'ease-in-out',
  })
  setTimeout(() =>{
    loading.value = false;
  }, 800);
});

</script>