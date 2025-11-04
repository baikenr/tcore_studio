<template>
  <article
    class="w-full max-w-[520px] rounded-[20px] p-10
           flex flex-col justify-between
           text-[#CFCEDF] text-[18px] sm:text-[20px] leading-[28px] tracking-[0.01em] font-medium
           shadow-[0_20px_60px_rgba(0,0,0,0.25)]
           bg-gradient-to-br from-white/5 via-white/3 to-white/1"
  >
    <p class="overflow-hidden text-ellipsis line-clamp-5">
      {{ text }}
    </p>

    <button
      class="mt-8 h-[56px] w-full sm:w-[260px] rounded-[16px]
             px-8 flex items-center justify-center
             transition duration-200 ease-out select-none
             hover:-translate-y-[1px] hover:shadow-[0_10px_30px_rgba(0,0,0,.25)]
             active:translate-y-0 active:scale-[0.99]
             bg-gradient-to-br from-white/10 via-white/5 to-white/3 border border-transparent"
    style="margin-top: 30px;"
             >
      <span
        class="text-[18px] sm:text-[20px] font-semibold leading-[100%]
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
