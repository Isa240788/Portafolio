<template>
  <section class="relative py-32 overflow-hidden bg-[#0a0f1d]" id="proyectos">
    <!-- 🌌 LUZ ROSA DE FONDO -->
    <div class="absolute top-0 left-1/2 -translate-x-1/2 w-250 h-150 bg-pink-500/5 rounded-full blur-[160px] z-0"></div>

    <div class="max-w-7xl mx-auto px-6 relative z-10">
      
      <!-- 📢 ENCABEZADO -->
      <div class="mb-20 text-center" data-aos="fade-up">
        <h2 class="text-5xl md:text-7xl font-black tracking-tighter italic uppercase leading-none text-white">
          PROYECTOS <span class="text-pink-500 not-italic">DESTACADOS</span>
        </h2>
        <p class="text-[10px] font-black uppercase tracking-[0.5em] text-pink-400 mt-4 opacity-80">Selección de Soluciones Reales | 2025-2026</p>
      </div>

      <!-- 🃏 GRID DE PROYECTOS (Solo los mejores, como pidió el profe) -->
      <div class="grid md:grid-cols-2 gap-12">
        
        <!-- PROYECTO 1: FINCHTECH -->
        <div class="group relative" data-aos="fade-right">
          <div class="card bg-gray-900 shadow-2xl rounded-[40px] overflow-hidden border border-white/10 hover:border-pink-500/50 transition-all duration-700">
            <figure class="relative h-72 overflow-hidden">
              <!-- Reemplaza con tu captura real de FinchTech -->
              <img src="../assets/finchtech-preview.png" alt="FinchTech Journal" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
              <div class="absolute inset-0 bg-gradient-to-t from-gray-900 via-transparent to-transparent opacity-80"></div>
              <div class="absolute top-6 left-6 flex gap-2">
                <span class="badge bg-white/10 backdrop-blur-md text-white border-none font-black text-[9px] uppercase tracking-widest px-4 py-3 rounded-2xl">Full-Stack</span>
                <span class="badge bg-white/10 backdrop-blur-md text-white border-none font-black text-[9px] uppercase tracking-widest px-4 py-3 rounded-2xl">Firebase</span>
              </div>
            </figure>
            
            <div class="card-body p-10">
              <h3 class="text-3xl font-black italic tracking-tighter text-white uppercase group-hover:text-pink-500 transition-colors">FinchTech Journal</h3>
              <p class="text-sm font-medium text-gray-400 leading-relaxed italic mt-4">
                Plataforma de inteligencia financiera con noticias en tiempo real sincronizadas con Firestore. Incluye autenticación robusta, sistema de comentarios y una arquitectura validada con Vitest.
              </p>
              
              <div class="card-actions justify-start mt-8 gap-4">
                <a href="https://github.com/Isa240788/mi-crypto-dash" target="_blank" class="btn btn-ghost btn-sm text-[10px] font-black uppercase tracking-widest text-white/40 hover:text-white transition-all">GitHub ➜</a>
                <a href="https://mi-crytpo-dash.vercel.app" target="_blank" class="btn btn-primary btn-sm rounded-xl px-8 font-black uppercase text-[10px] tracking-widest border-none shadow-lg shadow-pink-500/20 text-white">Demo Live</a>
              </div>
            </div>
          </div>
        </div>

        <!-- PROYECTO 2: METEOVITE -->
        <div class="group relative" data-aos="fade-left" data-aos-delay="200">
          <div class="card bg-gray-900 shadow-2xl rounded-[40px] overflow-hidden border border-white/10 hover:border-pink-500/50 transition-all duration-700">
                <figure class="relative h-72 overflow-hidden">
                <!-- Reemplaza con tu captura real de MeteoVite -->
                <img src="../assets/meteovite-preview.png" alt="MeteoVite Pro" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
                <div class="absolute inset-0 bg-gradient-to-t from-gray-900 via-transparent to-transparent opacity-80"></div>
                <div class="absolute top-6 left-6 flex gap-2">
                    <span class="badge bg-white/10 backdrop-blur-md text-white border-none font-black text-[9px] uppercase tracking-widest px-4 py-3 rounded-2xl">API Integration</span>
                </div>
                </figure>
                
                <div class="card-body p-10">
                <h3 class="text-3xl font-black italic tracking-tighter text-white uppercase group-hover:text-pink-500 transition-colors">MeteoVite Pro</h3>
                <p class="text-sm font-medium text-gray-400 leading-relaxed italic mt-4">
                    Dashboard meteorológico de alto rendimiento. Utiliza Geolocalización nativa y la API de Open-Meteo para visualización de datos climáticos dinámicos con una interfaz optimizada.
                </p>
                
                <div class="card-actions justify-start mt-8 gap-4">
                        <a href="https://github.com/Isa240788/proApp-vue-clima" target="_blank" class="btn btn-ghost btn-sm text-[10px] font-black uppercase tracking-widest text-white/40 hover:text-white transition-all">GitHub ➜</a>
                        <a href="https://m6l2pro-vue-clima.vercel.app/" target="_blank" class="btn btn-primary btn-sm rounded-xl px-8 font-black uppercase text-[10px] tracking-widest border-none shadow-lg shadow-pink-500/20 text-white">Demo Live</a>
                </div>
                </div>
            </div>
        </div>

        <!-- PROYECTO 3: SPA CON VUE -->
        <div class="group relative" data-aos="fade-right">
          <div class="card bg-gray-900 shadow-2xl rounded-[40px] overflow-hidden border border-white/10 hover:border-pink-500/50 transition-all duration-700">
                <figure class="relative h-72 overflow-hidden">
                <!-- Reemplaza con tu captura real de MeteoVite -->
                <img src="../assets/landing-preview.png" alt="MeteoVite Pro" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
                <div class="absolute inset-0 bg-gradient-to-t from-gray-900 via-transparent to-transparent opacity-80"></div>
                <div class="absolute top-6 left-6 flex gap-2">
                    <span class="badge bg-white/10 backdrop-blur-md text-white border-none font-black text-[9px] uppercase tracking-widest px-4 py-3 rounded-2xl">Vuejs</span>
                </div>
                </figure>
                
                <div class="card-body p-10">
                <h3 class="text-3xl font-black italic tracking-tighter text-white uppercase group-hover:text-pink-500 transition-colors">SPA Ferretería</h3>
                <p class="text-sm font-medium text-gray-400 leading-relaxed italic mt-4">
                    Landing page desarrollada con Vue 3 para una ferretería, enfocada en mostrar productos y categorías de forma clara, moderna y responsiva.
                </p>
                
                <div class="card-actions justify-start mt-8 gap-4">
                        <a href="https://github.com/Isa240788/Landing-page-ferreteria" target="_blank" class="btn btn-ghost btn-sm text-[10px] font-black uppercase tracking-widest text-white/40 hover:text-white transition-all">GitHub ➜</a>
                        <a href="https://landing-page-ferreteria.vercel.app/" target="_blank" class="btn btn-primary btn-sm rounded-xl px-8 font-black uppercase text-[10px] tracking-widest border-none shadow-lg shadow-pink-500/20 text-white">Demo Live</a>
                </div>
                </div>
            </div>
        </div>

      </div>
    </div>
  </section>
</template>
