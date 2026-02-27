<template>
   <div class="min-h-screen bg-linear-to-br from-gray-900 via-blue-900 to-gray-900">  
      <Navbar />
      <Hero />
      <About/>
      <Services/>
  </div> 
</template>

<script setup>
import { ref, onMounted, nextTick } from 'vue';
import Aos from 'aos';
import 'aos/dist/aos.css';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Services from './components/Services.vue';



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

<style scoped>

</style>