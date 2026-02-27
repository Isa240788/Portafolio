<template>
    <section class="relative py-12" id="habilidades">
        <div class="relative z-10 max-w-5xl mx-auto px-4 text-center">
            
            <h2 class="text-2xl font-bold text-white mb-10 tracking-tight" data-aos="fade-up">
                Habilidades
            </h2>         

            <!-- Grid fluido: 2 en móvil, 4 en tablet, 6 en desktop -->
            <div class="grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-6 gap-3">
                
                <div v-for="skill in skills" 
                     :key="skill.id" 
                     data-aos="zoom-in"
                     class="group flex flex-col items-center justify-center p-3 rounded-xl 
                            bg-gray-800/30 border border-gray-700/40 
                            hover:bg-gray-800/60 hover:border-rose-500/30 
                            transition-all duration-300">
                    
                    <!-- Icono Centrado -->
                    <div class="mb-2 transition-transform duration-300 group-hover:scale-110">
                        <FontAwesomeIcon 
                            :icon="skill.Icon" 
                            :class="[skill.iconColor, 'text-2xl w-7 h-7']" 
                        />
                    </div>

                    <!-- Nombre de la Tecnología -->
                    <span class="text-xs font-semibold text-gray-300 group-hover:text-white uppercase tracking-wider">
                        {{ skill.title }}
                    </span>

                </div> <!-- Fin Card Mini -->
            </div>
        </div>
    </section>
</template>


<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
// Importamos los objetos reales de los iconos
import { 
    faBootstrap, 
    faVuejs, 
    faHtml5, 
    faCss3Alt, 
    faSquareJs 
} from '@fortawesome/free-brands-svg-icons'

const skills = [
    {
        id: 1,
        title: "Bootstrap",
        Icon: faBootstrap, // Referencia al objeto importado arriba
        iconColor: 'text-purple-500',
    },
    {
        id: 2,
        title: "Vue",
        Icon: faVuejs,
        iconColor: 'text-emerald-400',
    },
    {
        id: 3,
        title: "HTML5", 
        Icon: faHtml5,
        iconColor: 'text-orange-500',
    },
    {
        id: 4,
        title: "CSS3", 
        Icon: faCss3Alt,
        iconColor: 'text-blue-500',
    },
    {
        id: 5,
        title: "JavaScript", 
        Icon: faSquareJs,
        iconColor: 'text-yellow-400',
    }
]
</script>

