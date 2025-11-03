<script setup lang="ts">
const props = defineProps<{
  title?: string
  lines?: string[]
  ctaText?: string
  ctaTo?: string
}>()

import { useScrollTo } from '@/composables/useScrollTo'
const { to } = useScrollTo()

const onClick = () => {
  if (props.ctaTo) to(props.ctaTo)
}
</script>

<template>
  <div class="hero__content">
    <h1 class="hero__title">{{ title ?? 'ItCore studio' }}</h1>

    <p class="hero__subtitle">
      <template v-for="(line, i) in (lines ?? [])" :key="i">
        {{ line }}<br />
      </template>
    </p>

    <button class="hero__btn" @click="onClick">
      {{ ctaText ?? 'Связаться' }}
    </button>
  </div>
</template>

<style scoped>
.hero__content {
  position: absolute;
  z-index: 4;
  left: clamp(24px, 5vw, 96px);
  bottom: clamp(28px, 9vh, 140px);
  max-width: min(820px, 60vw);
  font-family: 'Montserrat', sans-serif;
}

.hero__title {
  font-size: clamp(40px, 7.5vw, 96px);
  font-weight: 800;
  margin: 0 0 40px;
  line-height: 1.05;
}

.hero__subtitle {
  font-size: clamp(15px, 1.8vw, 20px);
  line-height: 1.6;
  color: rgba(255, 255, 255, .80);
  margin: 0 0 40px;
}

.hero__btn {
  background: transparent;
  color: #fff;
  border: 3px solid #fff;
  padding: 14px 38px;
  font-size: 20px;
  cursor: pointer;
  transition: .2s ease;
  font-family: 'Montserrat', sans-serif;
}
.hero__btn:hover {
  background: #fff;
  color: #000;
}
</style>
 