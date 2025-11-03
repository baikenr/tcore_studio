<template>
  <article
    class="group relative overflow-hidden rounded-[10px] border
           flex flex-col
           shadow-[0_20px_60px_rgba(0,0,0,.25)]
           transition-[transform,box-shadow,opacity] duration-300 ease-out
           will-change-[transform,box-shadow]
           hover:-translate-y-2 hover:shadow-[0_30px_80px_rgba(0,0,0,.35)]
           active:translate-y-0 active:scale-[0.99]"
    :class="addon
      ? 'bg-[#0C0C0C] text-white border-white/10'
      : 'bg-[#FFF4E6] text-[#111] border-black/10'"
    style="width:391px; height:653px;"
  >
    <!-- мягкое свечение при наведении -->
    <div
      class="pointer-events-none absolute inset-0 opacity-0
             transition-opacity duration-300 group-hover:opacity-100"
      :class="addon ? 'bg-white/[.06]' : 'bg-black/[.04]'"
    />

    <!-- бейдж ADD-ON -->
    <div
      v-if="addon"
      class="absolute top-[19px] left-[27px] px-[10px] py-[4px] text-[12px]
             rounded-[6px] border-black/10 bg-white text-black font-semibold"
    >
      ADD-ON
    </div>

    <!-- контент -->
    <div class="px-[44px] pt-[55px] pb-0 flex-1 flex flex-col">
      <!-- Заголовок + подзаголовок -->
      <div>
        <h3 class="font-extrabold leading-[145%] tracking-[0.02em] text-[30px]">
          {{ title }}
        </h3>

        <p
          v-if="subtitle"
          class="mt-[6px] text-[14px] leading-[145%] tracking-[0.02em]"
          :class="addon ? 'text-white/70' : 'text-[#4A4A4A]'"
        >
          {{ subtitle }}
        </p>
      </div>

      <!-- Цена -->
      <div v-if="price || priceNote" class="mt-[18px]">
        <div v-if="price" class="text-[40px] font-extrabold leading-[145%] tracking-[0.02em]">
          {{ price }}
        </div>
        <div
          v-if="priceNote"
          class="text-[14px] leading-[145%] tracking-[0.02em] mt-[2px]"
          :class="addon ? 'text-white/70' : 'text-[#4A4A4A]'"
        >
          {{ priceNote }}
        </div>
      </div>

      <!-- Что входит -->
      <div v-if="features?.length" class="mt-[24px]">
        <h4 class="text-[20px] font-bold leading-[145%] tracking-[0.02em] mb-[10px]">
          Что входит?
        </h4>

        <ul class="space-y-[8px] text-[14px] leading-[145%] tracking-[0.02em]">
          <li v-for="(f, i) in features" :key="i" class="flex gap-[10px] items-start">
            <span
              class="mt-[7px] inline-block w-[6px] h-[6px] rounded-full"
              :class="addon ? 'bg-white' : 'bg-black'"
            />
            <span>{{ f }}</span>
          </li>
        </ul>
      </div>

      <!-- заполнитель чтобы кнопки уехали вниз -->
      <div class="flex-1"></div>

      <!-- Кнопки -->
      <div class="pb-[22px] pt-[18px] flex flex-col items-center gap-[10px]">
        <!-- основная кнопка -->
        <button
          v-if="ctaPrimary"
          class="rounded-full text-[13px] font-bold tracking-[0.02em]
                 flex items-center justify-center select-none
                 transition-all duration-200 ease-out
                 hover:-translate-y-[1px] hover:shadow-[0_10px_30px_rgba(0,0,0,.25)]
                 active:translate-y-0 active:scale-[0.99]
                 focus:outline-none focus-visible:ring-2 focus-visible:ring-white/30"
          :class="addon
            ? 'text-white bg-transparent border border-white/60 hover:bg-white/10'
            : 'text-white bg-black hover:bg-white hover:text-black border border-transparent'"
          style="width:252px;height:41px;"
        >
          {{ ctaPrimary }}
        </button>

        <!-- вторичная кнопка -->
        <div
          class="flex flex-col items-center"
          :class="ctaSecondary ? '' : 'invisible pointer-events-none'"
          style="height:32px;"
        >
          <button
            class="text-[13px] font-bold tracking-[0.02em]
                   transition-opacity duration-150 hover:opacity-80
                   focus:outline-none focus-visible:ring-2 focus-visible:ring-white/20"
            :class="addon ? 'text-white' : 'text-black'"
          >
            {{ ctaSecondary }}
          </button>

          <!-- подчёркивание с лёгким «ростом» -->
          <div
            class="mt-[6px] h-[2px] origin-center transition-transform duration-200
                   group-hover:scale-x-105"
            :class="addon ? 'bg-white/90' : 'bg-black/90'"
            style="width:111px;"
          />
        </div>
      </div>
    </div>
  </article>
</template>

<script setup lang="ts">
const popularStyle = {
  background:
    'linear-gradient(90.03deg, #A800F5 -31.68%, #EDA4FF 10.37%, #FFE9CA 41.52%, #FFD5C5 75.79%, #FFC889 124.85%)'
}

defineProps<{
  title: string
  subtitle?: string
  price?: string
  priceNote?: string
  features?: string[]
  ctaPrimary?: string
  ctaSecondary?: string
  addon?: boolean
  popular?: boolean
}>()
</script>
