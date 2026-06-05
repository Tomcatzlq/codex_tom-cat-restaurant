<template>
  <section id="ambiance" style="padding-top:120px;padding-bottom:120px;">
    <div class="ambiance-section">
      <div class="ambiance-header reveal">
        <div class="section-label">餐厅空间</div>
        <h2 class="section-title serif">轻松、好看、有氛围</h2>
        <div class="gold-line"></div>
      </div>
      <div class="gallery-grid">
        <div v-for="item in gallery" :key="item.caption" class="gallery-item reveal">
          <img :src="item.image" :alt="item.caption" loading="lazy" />
          <div class="gallery-caption">{{ item.caption }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const gallery = [
  {
    caption: '主厅 · Main Dining',
    image: 'https://images.unsplash.com/photo-1559339352-11d035aa65de?w=900&q=80'
  },
  {
    caption: '吧台 · Bar Counter',
    image: 'https://images.unsplash.com/photo-1575037614876-c38a4d44f5b8?w=800&q=80'
  },
  {
    caption: '窗边�?· Window Seats',
    image: 'https://images.unsplash.com/photo-1551882547-ff40c63fe5fa?w=800&q=80'
  },
  {
    caption: '开放厨�?· Open Kitchen',
    image: 'https://images.unsplash.com/photo-1600891964092-4316c288032e?w=900&q=80'
  }
];
</script>
