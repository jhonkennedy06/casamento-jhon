<template>
  <div>
    <TheNavbar />
    <main>
      <HeroSection />
      <HistoriaSection />
      <PadrinhosSection />
      <PresentesSection />
    </main>
    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          <strong>Feito com ❤️ por Dayanne & Jhon Kennedy.</strong>
        </p>
      </div>
    </footer>

    <button
      v-show="showScrollToTopButton"
      class="scroll-to-top"
      @click="scrollToTop"
    >
      <span class="icon">
        <i class="fas fa-arrow-up"></i>
      </span>
    </button>

  </div>
</template>

<script lang="ts">
import { defineComponent, ref, onMounted, onUnmounted } from 'vue';
import TheNavbar from '@/components/TheNavbar.vue';
import HeroSection from '@/components/HeroSection.vue';
import PadrinhosSection from '@/components/PadrinhosSection.vue';
import HistoriaSection from '@/components/HistoriaSection.vue';
import PresentesSection from '@/components/PresentesSection.vue';

export default defineComponent({
  name: 'App',
  components: {
    TheNavbar,
    HeroSection,
    PadrinhosSection,
    HistoriaSection,
    PresentesSection,
  },
  setup() {
    const showScrollToTopButton = ref(false);

    const handleScroll = () => {
      if (window.scrollY > 300) {
        showScrollToTopButton.value = true;
      } else {
        showScrollToTopButton.value = false;
      }
    };

    const scrollToTop = () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    };
    onMounted(() => {
      window.addEventListener('scroll', handleScroll);
    });
    onUnmounted(() => {
      window.removeEventListener('scroll', handleScroll);
    });

    return {
      showScrollToTopButton,
      scrollToTop,
    };
  }
});
</script>

<style>
:root {
  --emerald-green: #2E8B57;
  --emerald-green-dark: #20603c;
  --text-color: #363636;
}
.title {
  color: var(--emerald-green) !important;
}
body {
  background-image: url('@/assets/background.png');
  background-position: center center;
  background-size: cover;
  background-attachment: fixed;
  background-color: #f5f5f5;
}

html {
  scroll-padding-top: 52px;
  scroll-behavior: smooth;
}
* {
  scrollbar-width: thin;
  scrollbar-color: var(--emerald-green) #f1f1f1;
}
::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background: #f1f1f1;
}
::-webkit-scrollbar-thumb {
  background-color: var(--emerald-green);
  border-radius: 20px;
  border: 2px solid #f1f1f1;
}
::-webkit-scrollbar-thumb:hover {
  background-color: var(--emerald-green-dark);
}
.scroll-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: var(--emerald-green);
  color: white;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  transition: opacity 0.3s ease-in-out, transform 0.3s ease-in-out;
}
.scroll-to-top:hover {
  background-color: var(--emerald-green-dark);
  transform: scale(1.1);
}
.footer {
  padding: 1.5rem;
  background-color: rgba(245, 245, 245, 0.9);
}
.footer p {
  color: var(--text-color);
}
strong {
  color: var(--emerald-green-dark);
  font-weight: 600;
}
</style>