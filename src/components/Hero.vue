<!-- En tu Hero.vue -->
<template>
  <section class="relative min-h-screen flex items-center overflow-hidden bg-[#0a0f1d]" id="inicio">
    
    <!-- 🌌 EL CIELO DE ISABEL (Aurora WebGL) -->
    <div class="absolute inset-0 z-0">
      <Aurora 
        :colorStops="['#f43f5e', '#8b5cf6', '#f43f5e']" 
        :amplitude="1.0"
        :speed="0.5"
        :intensity="0.9"
      />
    </div>

    <div class="max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-12 relative z-10 w-full pt-44 lg:pt-52 pb-20">
      <div data-aos="fade-right" class="order-2 lg:order-1">
        <!-- 👑 TEXTO EN BLANCO Y ROSA -->
        <h2 class="text-white font-black text-2xl md:text-4xl tracking-tighter uppercase italic opacity-90">
            HOLA, SOY
        </h2>
        <h1 class="font-black text-6xl md:text-8xl lg:text-9xl leading-none tracking-tighter uppercase italic drop-shadow-[0_0_15px_rgba(244,63,94,0.4)]">
          <span class="text-transparent bg-clip-text bg-linear-to-r from-pink-400 via-rose-500 to-pink-300 not-italic animate-pulse">
              ISABEL
          </span>
        </h1>

        <p class="text-white text-xl font-medium italic opacity-60 mt-6 max-w-md leading-relaxed">
          "Desarrolladora Front-End en formación, especializada en interfaces modernas y optimizadas."
        </p>
        
        <!-- 🔘 BOTONES ACTUALIZADOS -->
        <div class="flex flex-wrap gap-6 mt-12">
            <!-- 📧 BOTÓN CONTACTO (Lleva al id="contacto" en el footer) -->
            <a 
                href="#contacto" 
                class="btn btn-primary btn-lg rounded-3xl px-12 font-black uppercase text-[10px] tracking-[0.2em] border-none shadow-[0_0_20px_rgba(244,63,94,0.3)] hover:shadow-[0_0_40px_rgba(244,63,94,0.6)] hover:scale-105 transition-all duration-500 group relative overflow-hidden"
            >
                <span class="absolute inset-0 bg-white/20 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></span>
                <span class="relative flex items-center gap-2 text-white">
                  Contáctame 📧
                </span>
            </a>

            <!-- 🚀 VER PROYECTOS -->
            <a 
                href="#proyectos" 
                class="btn btn-outline btn-lg rounded-3xl px-12 font-black uppercase text-[10px] tracking-[0.2em] border-white/20 text-white hover:bg-white/5 hover:border-white hover:scale-105 transition-all duration-500 group"
            >
                Ver Proyectos
                <span class="group-hover:translate-x-2 transition-transform duration-300 ml-2">➜</span>
            </a>
        </div>
      </div>

      <!-- 👤 FOTO REDONDA -->
      <div class="flex justify-center lg:justify-end order-1 lg:order-2" data-aos="zoom-in">
        <div class="relative group">
            <div class="absolute -inset-2 bg-gradient-to-r from-primary to-rose-500 rounded-full blur opacity-20 group-hover:opacity-40 transition duration-700"></div>
            <div class="avatar">
                <div class="w-64 md:w-80 rounded-full ring ring-primary ring-offset-base-100 ring-offset-4 shadow-2xl overflow-hidden bg-neutral">
                    <img 
                      src="../assets/isa.jpg" 
                      alt="Isabel Guajardo" 
                      class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-700 hover:scale-110"
                    />
                </div>
            </div>
            <div class="absolute bottom-6 right-6 badge badge-primary p-3 border-none shadow-lg animate-pulse">
                <span class="text-[8px] font-black uppercase tracking-widest text-white">Online</span>
            </div>
        </div>
      </div>
    </div>
  </section>
</template>


<script setup>
import Aurora from './Aurora.vue'; // ✅ Asegúrate que la ruta sea correcta

// Usamos los iconos de 24/solid para que se vean más potentes
import { ArrowDownTrayIcon } from '@heroicons/vue/24/solid';
</script>
