<template>
   <section 
   class="relative w-full overflow-hidden min-h-screen flex items-center">
        <div 
        class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10">
            <div 
            class="flex flex-col md:mt-0 mt-20 justify-center">
                <div 
                class="text-white lg:text-left" data-aos="fade-right">
                    <h1 
                    class="text-white font-bold text-4xl md:text-5xl lg:text-6xl leading-tight">
                        Hola, soy 
                        <span class="text-transparent bg-clip-text bg-linear-to-r from-pink-400 to-rose-400">
                            Isabel
                        </span> 
                        👋
                    </h1>
                    <p 
                    class="text-blue-200 font-medium text-lg md:text-xl mt-4"
                    data-aos="fade-right"
                    data-aos-delay="100">
                        Desarrollador Front-End
                    </p>
                    <p 
                    class="text-blue-200 pt-6 text-justify  lg:text-left max-w-xl text-lg leading-relaxed"
                    data-aos="fade-right"
                    data-aos-delay="100">
                        Amante del Diseño, la música y programar.

                    </p>
                </div>

                <div 
                class="flex items-center gap-4 pt-10 flex-col sm:flex-row sm:w-max lg:mx-0"
                data-aos="fade-up"
                data-aos-delay="300">
                    <button
                    class="px-8 md:px-10 py-4 rounded-xl relative group w-full sm:w-max flex justify-center overflow-hidden bg-linear-to-r from-pink-600 to-rose-600 hover:from-pink-500 hover:to-rose-500 transition-all duration-300">
                        <span 
                        class="relative flex items-center justify-center text-white font-semibold text-lg">
                            Contactame
                            <ArrowRightIcon 
                            class="ml-2 w-5 h-5 group-hover:translate-x-1 transition-transform"/>
                        </span>
                    </button>
                    <button
                    class="border-blue-400 px-8 md:px-10 py-4 rounded-xl relative group w-full sm:w-max flex justify-center hover:bg-rose-400/10 transition-all duration-300">
                        <div 
                        class="flex items-center justify-center relative">
                            <ArrowDownTrayIcon 
                            class="w-5 h-5 text-white group-hover:translate-y-1 transition-transform"/>
                            <span 
                            class="pl-3 text-white font-semibold text-lg">
                               Descargar CV
                            </span>
                        </div>
                    </button>
                </div>

            </div>
        </div>
   </section>
</template>

<script setup>
import { ArrowDownTrayIcon, ArrowRightIcon } from '@heroicons/vue/16/solid';

</script>

<style scoped>

</style>