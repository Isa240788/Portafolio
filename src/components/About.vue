<template>
    <section
    class="relative py-20 overflow-hidden min-h-screen flex items-center"
    id="sobreMi">
        <div
        class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10">
            <div
            class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
                <div 
                class="text-center lg:text-left"
                data-aos="fade-left">
                    <h2
                    class="text-white font-bold text-4xl md:text-5xl lg:text-6xl leading-tight">
                        Sobre 
                        <span
                        class="text-transparent bg-clip-text bg-linear-to-r from-pink-400 to-rose-400">
                            Mi
                        </span>
                    </h2>
                    <p
                    class="text-white  font-medium text-lg md:text-xl mt-4"
                    data-aos="fade-left"
                    data-aos-delay="100">
                        Desarrollador Front-End
                    </p>
                </div>
                <p
                class="text-white pt-6 text-justify lg:text-left text-lg leading-relaxed"
                data-aos="fade-left"
                data-aos-delay="200">
                    Comencé como autodidacta aprendiendo marketing y diseño gráfico. Descubrí mi pasión por el diseño web en el instituto estudiando técnico en diseño, donde tenía asignaturas de programación y diseño plataformas digitales.<br/>
                    Esto me llevó a seguir aprendiendo de forma autónoma hasta llegar a la certificación de "TALENTO DIGITAL" impartida por Sence durante la temporada 2025-2026.              
                </p>
            </div>
            <div
            class="flex gap-4 pt-8 flex-col sm:flex-row"
            data-aos="fade-up"
            data-aos-delay="400">
                <button
                v-for="button in ctaButtons"
                :key="button.id"
                class="px-8 py-3 rounded-xl font-semibold transition-all duration-300 flex items-center justify-center"
                :class="button.classes">
                    <component 
                    :is="button.icon"
                    class="w-4 h-4"
                    :class="button.iconclass"/>
                        {{ button.text }}
                </button>
            </div>
        </div>

    </section>
</template>

<script setup>
import { ArrowRightIcon,ChatBubbleLeftRightIcon } from '@heroicons/vue/16/solid';


const ctaButtons =[
    {
        id: 1,
        text:'Ver Portafolio',
        icon: ArrowRightIcon,
        iconclass : `ml-2 group-hover:translate-x-1 transition-transform`,
        classes : `bg-linear-to-r from-pink-600 to-rose-600 text-white hover:from-pink-500 hover:to-rose-500`
    },
    {
        id: 2,
        text:'Contactame',
        icon: ChatBubbleLeftRightIcon,
        iconclass : `mr-2`,
        classes : `border border-pink-400 text-white hover:bg-rose-400/10`
    }
]
</script>
