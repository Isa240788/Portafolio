<template>
  <section class="relative py-32 bg-[#0a0f1d] overflow-hidden" id="trayectoria">
    <!-- 🌌 LUZ ROSA DE FONDO (Contraste Elle Woods) -->
    <div class="absolute top-0 right-0 w-150 h-150 bg-pink-500/10 rounded-full blur-[130px] z-0"></div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="grid lg:grid-cols-[1.2fr_2fr] gap-16 items-start">
        
        <!-- 🎭 LADO IZQUIERDO: EL TITULAR Y FORMACIÓN -->
        <div class="space-y-6" data-aos="fade-right">
          <h2 class="text-5xl md:text-7xl font-black tracking-tighter uppercase italic leading-none text-white">
            TRAYEC<span class="text-pink-500 not-italic">TORIA</span>
          </h2>
          
          <div class="badge badge-primary bg-pink-600 border-none p-4 font-black uppercase text-[10px] tracking-[0.3em] text-white shadow-lg shadow-pink-500/20">
            Frontend Developer & Educator
          </div>

          <!-- 🎓 STACK DE FORMACIÓN (DaisyUI Stats Style) -->
          <div class="space-y-4 mt-10">
            
            <!-- TARJETA 1: CURSO SENCE (El Protagonista) -->
            <div class="card bg-gray-900 shadow-2xl rounded-3xl p-5 border border-pink-500/50 group hover:scale-105 transition-all">
              <div class="flex items-center gap-4">
                <div class="w-12 h-12 rounded-xl bg-pink-500/20 flex items-center justify-center text-2xl group-hover:bg-pink-500 transition-colors">💻</div>
                <div>
                  <h4 class="text-[9px] font-black uppercase tracking-widest text-pink-400 italic">Hito Actual 2026</h4>
                  <p class="text-sm font-bold text-white uppercase leading-tight">Desarrollo de Aplicaciones Front-End Trainee</p>
                  <p class="text-[9px] font-medium text-white/50 uppercase tracking-tighter italic">Talento Digital (Sence)</p>
                </div>
              </div>
            </div>

            <!-- TARJETA 2: UDLA (Tu base profesional) -->
            <div class="card bg-gray-900 shadow-2xl rounded-3xl p-5 border border-white/10 group hover:scale-105 transition-all opacity-80">
              <div class="flex items-center gap-4">
                <div class="w-12 h-12 rounded-xl bg-blue-500/20 flex items-center justify-center text-2xl group-hover:bg-blue-500 transition-colors">🏃‍♀️</div>
                <div>
                  <h4 class="text-[9px] font-black uppercase tracking-widest text-blue-400">Título Profesional 2011</h4>
                  <p class="text-sm font-bold text-white italic">Pedagogía en Ed. Física</p>
                  <p class="text-[9px] font-medium text-white/50 uppercase tracking-tighter">Univ. de las Américas</p>
                </div>
              </div>
            </div>

          </div>
        </div>

        <!-- 📝 LADO DERECHO: TU HISTORIA (Súper Legible) -->
        <div class="space-y-8" data-aos="fade-left" data-aos-delay="200">
          <div class="prose prose-invert max-w-none">
            <p class="text-xl font-bold text-white leading-relaxed italic border-l-4 border-pink-500 pl-6 py-2 bg-pink-500/5 rounded-r-xl">
              "Una evolución profesional impulsada por la pedagogía, el diseño y la tecnología avanzada."
            </p>
            
            <div class="space-y-6 text-lg text-gray-100 leading-relaxed font-medium text-justify">
              <p>
                Titulada de Pedagogía en Educación Física (UDLA), poseo una base sólida en liderazgo y gestión de proyectos. Mi transición al desarrollo de software es el resultado de mi pasión por el Marketing y el Diseño Gráfico, encontrando en el código la herramienta perfecta para materializar soluciones digitales con propósito.
              </p>
              <p>
                Actualmente, consolido mi formación técnica en el curso de Desarrollo de Aplicaciones Front-End Trainee impartido por Talento Digital (Sence). Esta especialización intensiva me ha permitido dominar ecosistemas modernos como Vue.js y potenciar mi experiencia previa en la gestión de contenidos y bases de datos.
              </p>
            </div>
          </div>

          <!-- 🔘 BOTONES CON CONTRASTE 7.0 -->
          <div class="flex gap-4 pt-6 flex-col sm:flex-row justify-center lg:justify-start">
            <a href="#proyectos" class="btn bg-pink-600 hover:bg-pink-500 text-white rounded-2xl px-12 font-black uppercase text-[10px] tracking-widest border-none shadow-xl shadow-pink-500/30 transition-all scale-105">Ver Portafolio ➜</a>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
