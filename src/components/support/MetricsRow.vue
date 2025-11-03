<template>
  <div class="metrics" role="group" aria-label="Метрики поддержки">
    <div class="metric">
      <div class="num">200K</div>
      <div class="cap">
        A worldwide user<br />
        every month
      </div>
    </div>

    <div class="metric">
      <div class="num">85%</div>
      <div class="cap">
        Successfully solved<br />
        problems
      </div>
    </div>
  </div>
</template>

<style scoped>
.metrics{
  position: absolute;
  left: 98px;
  bottom: 36px;
  display: flex; gap: 48px;
}
.metric{ display:flex; flex-direction:column; gap: 6px; }
.num{
  font-size: 54px;
  font-weight: 800;
  letter-spacing: 0.02em;
}
.cap{
  font-size: 12px;
  line-height: 1.2;
  color: rgba(255,255,255,.75);
}
</style>
