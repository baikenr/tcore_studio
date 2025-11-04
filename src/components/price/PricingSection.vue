<template>
  <section class="relative w-full flex justify-center items-center py-20 sm:py-28 md:py-40 text-white"
    style="font-family: 'Manrope', sans-serif;">
    <img src="@/assets/images/pricing.png" alt=""
      class="absolute inset-0 w-full h-full object-cover opacity-70 -z-[2]" />

    <div
      class="relative z-[1] w-[95%] max-w-[1739px] rounded-[20px] border border-black bg-black/50 px-6 sm:px-10 md:px-20 py-10 sm:py-16 md:py-20">
      <h2 class="text-center font-bold tracking-[0.02em] leading-[130%]
               text-[32px] sm:text-[40px] md:text-[48px] lg:text-[55px] mb-4" style="margin-bottom: 30px;">
        Выберите тариф
      </h2>

      <p class="text-center text-white/90 tracking-[0.02em] leading-[145%]
         text-[16px] sm:text-[18px] md:text-[20px] lg:text-[24px]
         max-w-[850px] mx-auto" style="margin: 0 auto 60px; text-align: center;">
        Текст текстТекст текстТекст текстТекст текстТекст текстТекст текст
      </p>

      <div class="relative grid gap-10 sm:gap-12 md:gap-16 lg:gap-[126px]
               grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 place-items-center" style="margin-top: 30px;">
        <PricingCard title="Стандарт" subtitle="Один активный запрос за раз" price="????/Месяц" price-note="Текст"
          :features="[
            'Average 48 hour delivery',
            'Unlimited users',
            'Easy credit-card payments',
            'Pause or cancel anytime',
            'Unlimited revisions',
            'Unlimited stock photos'
          ]" cta-primary="Начать" cta-secondary="Заказать звонок" />

        <div class="relative w-full flex justify-center">
          <PopularBadge class="absolute top-[-20px] sm:top-[-25px] z-10" />
          <PricingCard title="Оптимальный" subtitle="Удваивайте активный запрос одновременно" price="????/Месяц"
            price-note="Текст" :features="[
              'One active request at a time',
              'Average 48 hour delivery',
              'Unlimited users',
              'Easy credit-card payments',
              'Pause or cancel anytime',
              'Unlimited revisions',
              'Unlimited stock photos'
            ]" cta-primary="Начать" cta-secondary="Заказать звонок" />
        </div>

        <PricingCard addon title="Webflow Development"
          subtitle="С помощью Webflow development вы сможете быстрее создать лучший веб-сайт." price="????/Месяц"
          price-note="Have any Questions? Let`s Meet!" cta-secondary="Заказать звонок" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import PricingCard from './PricingCard.vue'
import PopularBadge from './PopularBadge.vue'
</script>
