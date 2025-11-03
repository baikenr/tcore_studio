<template>
  <section class="relative w-full flex justify-center py-[160px] text-white" style="font-family:'Manrope',sans-serif;">
    <!-- фон -->
    <img
      src="@/assets/images/pricing.png"
      alt=""
      class="absolute inset-0 w-full h-full object-cover opacity-55 -z-[2]"
    />

    <!-- контейнер с карточками -->
    <div class="relative -z-[1] border rounded-[20px] bg-black/50 border-black" style="width:1739px;height:940px;">
      <!-- заголовок -->
      <h2
        class="absolute left-1/2 -translate-x-1/2 text-center font-bold tracking-[0.02em]
               leading-[145%] text-[55px]"
        style="top:37px; width:604px;"
      >
        Выберите тариф
      </h2>

      <!-- подзаголовок -->
      <p
        class="absolute left-1/2 -translate-x-1/2 text-center text-white/90
               tracking-[0.02em] leading-[145%] text-[24px]"
        style="top:119px; width:823px;"
      >
        Текст текстТекст текстТекст текстТекст текстТекст текстТекст текст
      </p>

      <!-- лента карточек -->
      <div
        class="absolute right-0 grid"
        style="
          top:198px;
          left:167px;
          width: calc(1739px - 167px - 167px);
          grid-template-columns: 391px 391px 391px;
          column-gap:126px;
        "
      >
        <PricingCard
          title="Стандарт"
          subtitle="Один активный запрос за раз"
          price="????/Месяц"
          price-note="Текст"
          :features="[
            'Average 48 hour delivery',
            'Unlimited users',
            'Easy credit-card payments',
            'Pause or cancel anytime',
            'Unlimited revisions',
            'Unlimited stock photos'
          ]"
          cta-primary="Начать"
          cta-secondary="Заказать звонок"
        />

        <!-- бейдж «Популярно» над средней карточкой -->
        <PopularBadge class="absolute left-[58%] -translate-x-1/2 -top-[18px] z-10" />

        <PricingCard
          title="Оптимальный"
          subtitle="Удваивайте активный запрос одновременно"
          price="????/Месяц"
          price-note="Текст"
          :features="[
            'One active request at a time',
            'Average 48 hour delivery',
            'Unlimited users',
            'Easy credit-card payments',
            'Pause or cancel anytime',
            'Unlimited revisions',
            'Unlimited stock photos'
          ]"
          cta-primary="Начать"
          cta-secondary="Заказать звонок"
        />

        <PricingCard
          addon
          title="Webflow Development"
          subtitle="С помощью Webflow development вы сможете быстрее создать лучший веб-сайт."
          price="????/Месяц"
          price-note="Have any Questions? Let`s Meet!"
          cta-primary="Заказать звонок"
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import PricingCard from './PricingCard.vue'
import PopularBadge from './PopularBadge.vue'
</script>
