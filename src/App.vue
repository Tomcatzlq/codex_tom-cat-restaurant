<template>
  <div>
    <NavBar />
    <HeroSection />
    <AboutSection />
    <div class="section-divider"></div>
    <DishesSection />
    <div class="section-divider"></div>
    <AmbianceSection />
    <div class="section-divider"></div>
    <MenuSection />
    <div class="section-divider"></div>
    <ChefSection />
    <div class="section-divider"></div>
    <ReservationSection />
    <SiteFooter />
  </div>
</template>

<script setup>
import { onMounted, onUnmounted } from 'vue';
import NavBar from './components/NavBar.vue';
import HeroSection from './components/HeroSection.vue';
import AboutSection from './components/AboutSection.vue';
import DishesSection from './components/DishesSection.vue';
import AmbianceSection from './components/AmbianceSection.vue';
import MenuSection from './components/MenuSection.vue';
import ChefSection from './components/ChefSection.vue';
import ReservationSection from './components/ReservationSection.vue';
import SiteFooter from './components/SiteFooter.vue';

let observer;

onMounted(() => {
  document.querySelector('.hero')?.classList.add('visible');

  observer = new IntersectionObserver(
    entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
          observer.unobserve(entry.target);
        }
      });
    },
    { threshold: 0.1 }
  );

  requestAnimationFrame(() => {
    document.querySelectorAll('.reveal').forEach(el => {
      const rect = el.getBoundingClientRect();
      if (rect.top < window.innerHeight && rect.bottom > 0) {
        el.classList.add('visible');
      } else {
        observer.observe(el);
      }
    });
  });
});

onUnmounted(() => {
  observer?.disconnect();
});
</script>