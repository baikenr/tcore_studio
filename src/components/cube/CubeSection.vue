<template>
  <section
    class="relative w-full min-h-screen overflow-hidden text-white"
    aria-label="Информационный блок"
    style="font-family:'Inter',sans-serif; background:rgba(4,6,17,1);"
  >
    <img
      src="@/assets/images/cube.png"
      alt=""
      class="absolute inset-0 w-full h-full object-cover opacity-30 z-[1]"
    />

    
    <div class="relative z-[2] pt-[60px]">
      <GlassField />
      <div class="h-[20px]"></div>
      <GlassTextCard />
    </div>
  </section>
</template>

<script setup lang="ts">
import GlassField from './GlassField.vue'
import GlassTextCard from './GlassTextCard.vue'
</script>
