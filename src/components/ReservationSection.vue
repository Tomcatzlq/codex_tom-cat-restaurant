<template>
  <section id="reservation" style="padding-top:120px;padding-bottom:120px;">
    <div class="reservation reveal">
      <div class="section-label">预约席位</div>
      <h2 class="section-title serif">周末和聚餐建议提前预约</h2>
      <div class="gold-line"></div>
      <p>汤姆猫餐厅适合朋友小聚、生日餐、轻松约会和小型庆祝。周末晚间较为热门，建议提前两到三天预约，以便我们为您保留合适的座位。</p>
      <div class="res-info">
        <div class="res-item">
          <div class="res-icon">●</div>
          <div class="res-label">餐厅地址</div>
          <div class="res-value">城市中心商业区 · 汤姆猫餐厅</div>
        </div>
        <div class="res-item">
          <div class="res-icon">●</div>
          <div class="res-label">营业时间</div>
          <div class="res-value">周一至周日 11:00 - 22:00</div>
        </div>
        <div class="res-item">
          <div class="res-icon">✓</div>
          <div class="res-label">预约电话</div>
          <div class="res-value">400-888-9999</div>
        </div>
      </div>
      <button class="res-btn" type="button" @click="onReserve">立即预约</button>
    </div>
  </section>
</template>

<script setup>
function onReserve() {
  window.alert('汤姆猫餐厅的在线预约系统即将上线，敬请期待！');
}
</script>
