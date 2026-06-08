<template>
  <section id="menu" class="menu-section" style="padding-top:120px;padding-bottom:120px;">
    <div class="menu-inner">
      <div class="menu-header reveal">
        <div class="section-label">季节菜单</div>
        <h2 class="section-title serif">夏日轻松吃喝指南</h2>
        <div class="gold-line"></div>
        <p>汤姆猫餐厅提供单点和双人分享套餐。推荐首次到店的客人先从招牌菜和季节限定中各选一道，再搭配一杯特调饮品。</p>
      </div>

      <div v-for="category in menu" :key="category.title" class="menu-category reveal">
        <div class="menu-cat-title serif">{{ category.title }}</div>
        <div v-for="item in category.items" :key="item.name" class="menu-item">
          <div class="menu-item-left">
            <div class="menu-item-name serif">{{ item.name }}</div>
            <div class="menu-item-en">{{ item.en }}</div>
          </div>
          <div class="menu-dots"></div>
          <div class="menu-item-price">{{ item.price }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const menu = [
  {
    title: '前菜 · 小食',
    items: [
      { name: '猫咪薯条拼盘', en: 'Tom Cat Fries Platter', price: '¥38' },
      { name: '香辣鸡翅篮', en: 'Spicy Chicken Wings', price: '¥48' },
      { name: '番茄芝士焗虾', en: 'Baked Tomato Cheese Shrimp', price: '¥68' }
    ]
  },
  {
    title: '主食 · 分享',
    items: [
      { name: '招牌牛肉汉堡', en: 'Signature Beef Burger', price: '¥78' },
      { name: '黑松露蘑菇饭', en: 'Black Truffle Mushroom Rice', price: '¥88' },
      { name: '炙烤猪肋排', en: 'Grilled Pork Ribs', price: '¥128' }
    ]
  },
  {
    title: '甜品 · 饮品',
    items: [
      { name: '海盐焦糖奶昔', en: 'Salted Caramel Milkshake', price: '¥38' },
      { name: '柚子气泡饮', en: 'Yuzu Sparkling Drink', price: '¥32' },
      { name: '巧克力熔岩蛋糕', en: 'Chocolate Lava Cake', price: '¥58' }
    ]
  }
];
</script>
