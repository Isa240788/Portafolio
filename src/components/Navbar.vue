<template>
  <!-- 🌊 CONTENEDOR MAESTRO: 'fixed' para que flote sobre la Aurora -->
  <header class="fixed top-6 w-full flex justify-center z-50 px-4 pointer-events-none">
    
    <!-- 🧊 LA CÁPSULA GLASSMORPHISM (Centrada y Horizontal) -->
    <nav class="pointer-events-auto flex items-center justify-between 
                w-full max-w-3xl h-16 px-8 rounded-full 
                backdrop-blur-md bg-white/5 border border-white/10 
                shadow-2xl transition-all duration-500">
      
      <!-- 🏢 LADO IZQUIERDO: TU MARCA -->
      <div class="flex-none">
        <div class="text-xl font-black tracking-tighter italic uppercase text-white cursor-pointer group">
          <a href="#inicio">DEV <span class="text-primary group-hover:text-pink-400 transition-colors">PORTAFOLIO</span></a>
        </div>
      </div>

      <!-- 💻 MENÚ DESKTOP: Solo las 4 secciones en una fila -->
      <div class="hidden md:flex flex-1 justify-end">
        <ul class="flex items-center gap-8">
          <li v-for="item in Menu" :key="item.name">
            <a :href="item.href" 
               @click.prevent="scrollToSection(item.href)"
               class="text-[10px] font-black uppercase tracking-[0.3em] text-white hover:text-pink-400 transition-color px-2">
              {{ item.name }}
            </a>
          </li>
        </ul>
      </div>

      <!-- 📱 MENÚ MÓVIL (Dropdown con Heroicons) -->
<!-- 📱 MENÚ MÓVIL (Con control total de Vue) -->
<div class="md:hidden flex-none relative">
    <!-- Botón con Icono Dinámico -->
    <button 
      @click="isMenuOpen = !isMenuOpen" 
      class="btn btn-ghost btn-circle text-white focus:bg-transparent active:bg-transparent"
    >
        <component 
          :is="isMenuOpen ? XMarkIcon : Bars3Icon" 
          class="h-6 w-6 transition-all duration-300"
        />
    </button>
    
    <!-- El menú con transiciones de Vue -->
    <transition name="fade-slide">
      <ul 
        v-if="isMenuOpen" 
        class="absolute top-16 right-0 p-4 shadow-2xl backdrop-blur-3xl bg-black/90 rounded-3xl w-64 border border-white/10 space-y-2 z-[100]"
      >
          <li v-for="item in Menu" :key="item.name">
              <a 
                :href="item.href" 
                @click="scrollToSection(item.href)" 
                class="flex font-bold uppercase text-[10px] tracking-widest text-white/80 py-4 px-4 hover:bg-pink-600 hover:text-white rounded-2xl transition-all duration-300"
              >
                  {{ item.name }}
              </a>
          </li>
      </ul>
    </transition>
</div>



    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue';
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/solid';
const Menu = ref([
    {name:'Trayectoria', href:'#trayectoria'},
    {name:'Expertise', href:'#expertis'},
    {name:'Proyectos', href:'#proyectos'} 
])

const isMenuOpen = ref(false);

const scrollToSection = (href) => {
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
    }
}
</script>

<style scoped>
.fade-slide-enter-active, .fade-slide-leave-active {
  transition: all 0.3s ease;
}
.fade-slide-enter-from, .fade-slide-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>