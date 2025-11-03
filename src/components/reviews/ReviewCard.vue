<template>
  <article
    class="w-[520px] h-[278px] rounded-[20px] p-[32px]
           flex flex-col justify-between
           text-[#CFCEDF] text-[20px] leading-[28px] tracking-[0.01em] font-medium
           shadow-[0_20px_60px_rgba(0,0,0,0.25)]"
    :style="{
      background:
        'linear-gradient(102.26deg, rgba(241,248,255,0.08) 0.14%, rgba(239,243,255,0.03) 99.86%)'
    }"
  >
    <p class="w-[456px] h-[156px] overflow-hidden text-ellipsis line-clamp-5">
      {{ text }}
    </p>

    <button
      class="mt-[32px] h-[56px] w-[260px] rounded-[16px]
             px-[32px] flex items-center justify-center
             transition duration-200 ease-out select-none
             hover:-translate-y-[1px] hover:shadow-[0_10px_30px_rgba(0,0,0,.25)]
             active:translate-y-0 active:scale-[0.99]"
      :style="{
        background:
          'linear-gradient(145.15deg, rgba(255,255,255,0.10) -0.77%, rgba(247,249,255,0.05) 47.68%, rgba(239,250,255,0.03) 97.08%)',
        border: '1px solid transparent'
      }"
    >
      <span
        class="text-[20px] font-semibold leading-[100%]
               bg-clip-text text-transparent
               [background-image:linear-gradient(135deg,#F1F8FE_0%,#DAECFF_51.92%,#CAE4FF_100%)]"
      >
        Читать полностью
      </span>
    </button>
  </article>
</template>

<script setup lang="ts">
defineProps<{ text: string }>()
</script>
