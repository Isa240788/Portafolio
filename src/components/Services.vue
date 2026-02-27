<template>
   <section 
   class="relative py-20 overflow-hidden" 
   id="servicios">
        <div 
        class="relative z-10 max-w-7xl mx-auto px-4 sm:px-8 lg:px-8">
            <div 
            class="text-center m-16" 
            data-aos="fade-up">
                <h2 
                class="text-4xl md:text-5xl font-bold text-white mb-4">
                    Mis 
                    <span 
                    class="text-transparent bg-clip-text bg-linear-to-r from-pink-400 to-rose-400">
                        Servicios
                    </span>
                </h2>
                <p 
                class="text-white text-lg max-w-2xl mx-auto" data-aos="fade-up" 
                data-aos-delay="100">
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. 
                </p>
            </div>
            <div 
            class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div 
                v-for="(service, index) in services" :key="service.id" 
                :data-aos="'fade-up'" 
                :data-aos-delay="(index * 100) + 200" 
                class="group relative p-8 rounded-2xl bg-linear-to-br from-gray-800/50 to-blue-900-30 backdrop-blur-sm borde border-blue-500/20 hover:border-blue-400/40 transition-all duration-500 hover:transform hover:-translate-y-2 ">
                    <div 
                    class="aboslute inset-0 bg-linear-to-r from-blue-500/5 to-cyan-500/5 rounded-2xl opacity-0 duration-500 group-hover:opacity-100 transition-opacity">
                    </div>
                    <div 
                    class="inline-flex items-center justify-center w-16 h-16 rounded-xl bg-linear-to-r from-blue-500/20 to-cyan-500/20 border border-rose-400/30 group:hover:scale-110 transition-transform duration-300">
                        <component 
                        :is="service.icon" 
                        class="text-rose-400 w-8 h-8 transition-colors duration-300 group-hover:text-white">
                        </component>
                    </div>
                    <div class="relative z-10">
                        <h3 
                        class="text-xl font-bold text-white mb-3 group-hover:text-rose-400 transition-colors duration-300">
                            {{ service.name }}
                        </h3>
                        <p
                        class="text-rose-100 leading-relaxed">
                            {{ service.desc }}
                        </p>
                    </div>
                    <div
                    class="absolute bottom-6 right-6 opacity-0 group-hover:opacity-100 transform translate-x-4 group-hover:translate-x-0 transition-all duration-300">
                        <ArrowRightIcon
                        class="w-6 h-6 text-rose-400"/>
                    </div>
                </div>

            </div>
            <div
            class="text-center mt-16"
            data-aos="fade-up"
            data-aos-delay="800">
                <div
                class="inline-flex flex flex-col sm:flex-row gap-4 items-center">
                    <button
                    class="px-8 py-4 rounded-xl border-2 border-rose-400 text-rose-400 font-semibold hover:bg-pink-400/10 hover:text-white transition-all duration-300 flex items-center">
                        Contacto
                        <ChatBubbleLeftRightIcon
                        class="w-5 h-5 ml-2"/>
                    </button>

                </div>
            </div>
        </div>

   </section>
</template>

<script setup>
import { ArrowRightIcon, ChatBubbleLeftRightIcon, CodeBracketIcon, ComputerDesktopIcon, DevicePhoneMobileIcon, DocumentTextIcon, EnvelopeIcon} from '@heroicons/vue/16/solid';
import { ref } from 'vue';

const services = ref([
    {
        id: 1,
        icon: CodeBracketIcon,
        name: 'Desarrollador Web',
        desc:`Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sed tempora cupiditate, fugiat architecto obcaecati dolor.`
    },
       {
        id: 2,
        icon: DocumentTextIcon,
        name: 'Lenguaje Técnico',
        desc: `Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sed tempora cupiditate, fugiat architecto obcaecati dolor.`
    },
       {
        id: 3,
        icon: ComputerDesktopIcon,
        name: 'Diseño Web',
        desc:`Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sed tempora cupiditate, fugiat architecto obcaecati dolor.`
    },
    {
        id: 4,
        icon: EnvelopeIcon,
        name: 'Email Marketing',
        desc: `Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sed tempora cupiditate, fugiat architecto obcaecati dolor.`
    }
])
</script>

<style scoped>

</style>