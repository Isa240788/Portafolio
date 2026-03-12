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
        <div class="md:hidden flex-none">
            <div class="dropdown dropdown-end">
                <label tabindex="0" class="btn btn-ghost btn-circle text-white" @click="isMenuOpen = !isMenuOpen">
                <!-- ✅ Usamos Heroicons para evitar errores de SVG manual -->
                    <component 
                    :is="isMenuOpen ? XMarkIcon : Bars3Icon" 
                    class="h-6 w-6 transition-all duration-300"
                    />
                </label>
                
                <!-- El menú Glassmorphism se mantiene igual de pro -->
                <ul v-if="isMenuOpen" tabindex="0" class="menu menu-sm dropdown-content mt-4 p-4 shadow-2xl backdrop-blur-3xl bg-black/80 rounded-3xl w-64 border border-white/10 space-y-2">
                    <li v-for="item in Menu" :key="item.name">
                        <a :href="item.href" @click="scrollToSection(item.href)" class="font-bold uppercase text-[10px] tracking-widest text-white/80 py-3  hover:bg-pink-600 hover:text-white hover:border-pink-500 hover:scale-110 cursor-default transition-all duration-300">
                            {{ item.name }}
                        </a>
                    </li>
                </ul>
            </div>
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
