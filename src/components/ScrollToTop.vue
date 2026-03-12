<template>
  <transition name="fade">
    <button 
      v-if="isVisible" 
      @click="scrollToTop"
      class="fixed bottom-8 right-8 z-100 btn btn-primary btn-circle shadow-[0_0_20px_rgba(244,63,94,0.4)] border-none hover:scale-110 hover:shadow-[0_0_40px_rgba(244,63,94,0.6)] transition-all duration-500 group"
    >
      <ChevronUpIcon class="w-6 h-6 text-white group-hover:-translate-y-1 transition-transform" />
    </button>
  </transition>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { ChevronUpIcon } from '@heroicons/vue/24/solid';

const isVisible = ref(false);

const checkScroll = () => {
  // Aparece después de bajar 400px
  isVisible.value = window.scrollY > 400;
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

onMounted(() => window.addEventListener('scroll', checkScroll));
onUnmounted(() => window.removeEventListener('scroll', checkScroll));
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: all 0.4s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
  transform: translateY(20px) scale(0.5);
}
</style>
