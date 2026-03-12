<template>
  <section class="relative py-32 overflow-hidden bg-[#0a0f1d]" id="expertis">
    <!-- 🌌 LUZ ROSA DE FONDO -->
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-200 h-200 bg-pink-500/10 rounded-full blur-[160px] z-0"></div>

    <div class="max-w-7xl mx-auto px-6 relative z-10">
      
      <!-- 📢 ENCABEZADO -->
      <div class="mb-20 text-center lg:text-left" data-aos="fade-up">
        <h2 class="text-5xl md:text-7xl font-black tracking-tighter italic uppercase leading-none text-white drop-shadow-sm">
          EXPERTISE & <span class="text-pink-500 not-italic animate-pulse">TOOLKIT</span>
        </h2>
        <p class="text-[10px] font-black uppercase tracking-[0.5em] text-pink-400 mt-4 opacity-80">Soluciones Técnicas | Stack Tecnológico 2026</p>
      </div>

      <div class="grid lg:grid-cols-[1.5fr_1fr] gap-10 items-start">
        
        <!-- 🛠️ LADO IZQUIERDO: SERVICIOS -->
        <div class="grid sm:grid-cols-2 gap-4" data-aos="fade-right">
          <div 
            v-for="service in services" :key="service.id" 
            class="card bg-gray-900 shadow-2xl rounded-4xl border border-white/10 p-8 group hover:border-pink-500/50 transition-all duration-500"
          >
            <div class="w-12 h-12 rounded-xl bg-pink-500/10 flex items-center justify-center mb-6 group-hover:bg-pink-600 transition-all">
              <component :is="service.icon" class="text-pink-400 w-6 h-6 group-hover:text-white" />
            </div>
            <h3 class="text-xl font-black text-white uppercase italic mb-3 group-hover:text-pink-500 transition-colors">
              {{ service.name }}
            </h3>
            <p class="text-xs font-bold text-gray-400 leading-relaxed italic group-hover:text-gray-100 transition-colors">
              {{ service.desc }}
            </p>
          </div>
        </div>

        <!-- 🧪 LADO DERECHO: TECH STACK + TAGS (Todo en una cápsula) -->
        <div class="card bg-gray-900 shadow-2xl rounded-[40px] p-8 border border-white/20" data-aos="fade-left">
          <div class="mb-8">
            <h4 class="text-xs font-black uppercase tracking-[0.3em] text-pink-500 italic mb-2">Tech Stack</h4>
            <p class="text-[9px] font-bold text-white uppercase tracking-tighter italic opacity-40">Herramientas & Ecosistemas</p>
          </div>
          
          <!-- Grid de Iconos -->
          <div class="grid grid-cols-2 sm:grid-cols-3 gap-3">
            <div v-for="skill in skills" :key="skill.title" 
                 class="group flex flex-col items-center justify-center p-5 rounded-2xl 
                        bg-[#0a0f1d] border border-white/10 
                        hover:border-pink-500/40 transition-all duration-500">
              
              <div class="mb-3 transition-transform duration-500 group-hover:scale-125">
                <FontAwesomeIcon 
                  :icon="skill.Icon" 
                  :class="`${skill.iconColor} text-3xl grayscale group-hover:grayscale-0 transition-all duration-500 drop-shadow-[0_0_8px_rgba(255,255,255,0.2)]`" 
                />
              </div>

              <span class="text-[9px] font-black uppercase text-white opacity-40 group-hover:opacity-100 group-hover:text-pink-400 tracking-widest text-center transition-all">
                {{ skill.title }}
              </span>
            </div>
          </div>

          <!-- 🏷️ SPECIAL TAGS (Dentro del div de skills con Hover Rosa) -->
          <div class="flex flex-wrap gap-2 pt-8 mt-8 border-t border-white/10 justify-center">
            <span v-for="tag in tags" :key="tag" 
                  class="badge badge-outline border-white/20 text-[8px] font-black uppercase text-white/40 px-3 py-3 
                        hover:rounded-2xl hover:bg-pink-600 hover:text-white hover:border-pink-500 hover:scale-110 cursor-default transition-all duration-300">
              {{ tag }}
            </span>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>


<script setup>
import { ref } from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { 
  CodeBracketIcon, ComputerDesktopIcon, DocumentTextIcon, EnvelopeIcon 
} from '@heroicons/vue/24/solid';
import { 
  faVuejs, faHtml5, faCss3Alt, faSquareJs, faBootstrap, faGitAlt 
} from '@fortawesome/free-brands-svg-icons';
import { faDatabase, faBezierCurve, faWind, faWandMagicSparkles, faWandSparkles } from '@fortawesome/free-solid-svg-icons';

const services = ref([
  { id: 1, icon: CodeBracketIcon, name: 'Desarrollo Web', desc: 'Interfaces reactivas con Vue.js 3, optimizadas para rendimiento.' },
  { id: 2, icon: ComputerDesktopIcon, name: 'Diseño UX/UI', desc: 'Plataformas intuitivas con estética moderna y funcional.' },
  { id: 3, icon: DocumentTextIcon, name: 'Gestión Contenido', desc: 'Administración de activos digitales para proyectos internacionales.' },
  { id: 4, icon: EnvelopeIcon, name: 'Marketing Digital', desc: 'Estrategia y gestión de comunidades en el entorno técnico.' }
]);

const skills =[
  { id: 1, title: "Bootstrap", Icon: faBootstrap, iconColor: 'text-purple-500'},
  { id: 2, title: "Vue", Icon: faVuejs, iconColor: 'text-emerald-400'},
  { id: 3, title: "HTML5", Icon: faHtml5, iconColor: 'text-orange-500'},
  { id: 4, title: "CSS3", Icon: faCss3Alt, iconColor: 'text-blue-500'},
  { id: 5, title: "JavaScript", Icon: faSquareJs, iconColor: 'text-yellow-400'},
  { id: 6, title: "Firebase", Icon: faDatabase, iconColor: 'text-yellow-500' },
  { id: 7, title: "Illustrator",  Icon: faBezierCurve, iconColor: 'text-orange-600' },
  { id: 8, title: "DaisyUI", Icon: faWandSparkles, iconColor: 'text-pink-400'},
  { id: 9, title: "Tailwind", Icon: faWind, iconColor: 'text-sky-400' }
];

const tags = ["Vitest", "Cypress", "Composition API", "Pinia", "SEO", "Responsive"];
</script>
