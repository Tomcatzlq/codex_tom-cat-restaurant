<template>
  <nav :class="{ scrolled }">
    <div class="nav-logo serif">汤姆猫餐厅<span>Tom Cat</span></div>
    <ul class="nav-links">
      <li><a href="#about">关于我们</a></li>
      <li><a href="#dishes">招牌菜品</a></li>
      <li><a href="#ambiance">餐厅空间</a></li>
      <li><a href="#menu">季节菜单</a></li>
      <li><a href="#chef">主厨团队</a></li>
      <li><a href="#reservation">预约席位</a></li>
    </ul>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const scrolled = ref(false);

function onScroll() {
  scrolled.value = window.scrollY > 80;
}

onMounted(() => window.addEventListener('scroll', onScroll));
onUnmounted(() => window.removeEventListener('scroll', onScroll));
</script>
