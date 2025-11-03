<script setup>
import HeroContent from './HeroContent.vue';
import { ChevronDown } from 'lucide-vue-next';
</script>

<template>
  <section
    class="relative w-full h-screen overflow-hidden bg-[#0b0b0c] text-white"
    aria-label="Hero section"
    style="font-family: 'Manrope', sans-serif;"
  >
    <img
      src="@/assets/images/hero-bg.png"
      alt="Фон"
      class="absolute inset-0 w-full h-full object-cover object-[50%_38%] z-[1]"
    />

    <div class="absolute right-0 top-0 flex w-[30%] h-full z-[3]">
      <div class="flex-1 bg-white/15 flex flex-col justify-end items-center pb-[40px]">
        <a
          href="#top"
          class="font-extrabold text-[22px] hover:text-gray-300 transition"
        >
          Главная
        </a>
      </div>
      <div class="flex-1 bg-[#2f2f2f]/15 flex flex-col justify-end items-center pb-[40px]">
        <a
          href="#contacts"
          class="font-extrabold text-[22px] hover:text-gray-300 transition"
        >
          Контакты
        </a>
      </div>
      <div class="flex-1 bg-black/15 flex flex-col justify-end items-center pb-[40px]">
        <a
          href="#portfolio"
          class="font-extrabold text-[22px] hover:text-gray-300 transition"
        >
          Портфолио
        </a>
      </div>
      <div class="flex-1 flex flex-col justify-between items-center py-2 relative">
        <img
          src="@/assets/images/ring.png"
          alt="Кольцо"
          class="p-6 scale-x-[1.1]"
        />

        <a
          href="#next-section"
          class="mb-3"
        >
          <ChevronDown class="w-20 h-25 text-white hover:text-gray-300 transition" />
        </a>
      </div>
    </div>

    <HeroContent
      class="absolute left-[87px] bottom-[20%] z-[5]"
      :title="'ItCore studio'"
      :lines="[
        'От лендинга до CRM — ItCore делает digital-решения под Ваш бизнес.',
        'Без шаблонов. Без воды. На результат.',
        'От лендинга до CRM — ItCore делает digital-решения под Ваш бизнес.',
        'Без шаблонов. Без воды. На результат.'
      ]"
      cta-text="Связаться"
      cta-to="#contacts"
    />
  </section>
</template>
