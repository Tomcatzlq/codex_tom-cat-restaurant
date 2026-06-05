<template>
  <section id="dishes" style="padding-top:120px;padding-bottom:120px;">
    <div class="dishes-section">
      <div class="dishes-header reveal">
        <div class="section-label">汤姆猫招牌</div>
        <h2 class="section-title serif">每一道都值得拍照</h2>
        <div class="gold-line"></div>
        <p>我们精选了最受客人欢迎的三道菜品：颜值高、口味稳、出餐快，是第一次来汤姆猫餐厅的首选。</p>
      </div>
      <div class="dish-grid">
        <div v-for="dish in dishes" :key="dish.name" class="dish-card reveal">
          <img :src="dish.image" :alt="dish.name" loading="lazy" />
          <div class="dish-info">
            <div class="dish-name serif">{{ dish.name }}</div>
            <div class="dish-en">{{ dish.en }}</div>
            <div class="dish-desc">{{ dish.desc }}</div>
            <div class="dish-price">{{ dish.price }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const dishes = [
  {
    name: '猫咪炙烤牛排',
    en: 'Tom Cat Grilled Steak',
    desc: '谷饲牛排现点现烤，搭配招牌黑蒜酱与时令蔬菜',
    price: '¥188',
    image: 'https://images.unsplash.com/photo-1544025162-d76694265947?w=800&q=80'
  },
  {
    name: '奶油蘑菇意面',
    en: 'Creamy Mushroom Pasta',
    desc: '三种蘑菇慢炒出香，搭配手工宽面和帕玛森芝士',
    price: '¥78',
    image: 'https://images.unsplash.com/photo-1555396273-367ea4eb4db5?w=800&q=80'
  },
  {
    name: '焦糖布蕾拼盘',
    en: 'Crème Brûlée Platter',
    desc: '香草、伯爵茶、柚子三种口味组合，适合分享',
    price: '¥68',
    image: 'https://images.unsplash.com/photo-1470324161839-ce2bb6fa6bc3?w=800&q=80'
  }
];
</script>

