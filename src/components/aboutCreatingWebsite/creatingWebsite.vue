<script setup>
import Diamond from "@/assets/images/diamond.svg";
import RightArrow from "@/assets/images/right_arrow.svg";

const mainContent = {
  title:
    "Создаем сайты под ключ для онлайн или оффлайн бизнеса. Формируем продающую структуру с высокой конверсией. Окупаемость вложений через месяц после запуска",
  text:
    "Разрабатываем сайты на Tilda «под ключ» с адаптивным дизайном. Создаём продающие сайты для бизнеса, которые окупают затраты через месяц после запуска. Анализируем маркетинговую составляющую продукта и внедряем триггерные компоненты, которые увеличивают конверсию.",
  link: "#",
};

const services = [
  {
    title: "Лендинг",
    text:
      "Длинная посадочная страница с конверсией от 4% для сбора контактов на регистрацию или покупку. Презентация и предложение вашего уникального продукта на одной странице с раскрытием преимуществ, необходимости продукта, установкой доверия между компанией, её продуктом и посетителем.",
    link: "#",
  },
  {
    title: "Корпоративный сайт",
    text:
      "Корпоративные сайты — крупные многостраничные ресурсы. Это имиджевый инструмент работы фирмы через интернет. На них размещают описание услуг, преимущества, продукцию, полную информацию для представительства в интернете.",
    link: "#",
  },
  {
    title: "Сайт-визитка",
    text:
      "Главная информация об организации и услугах с минимальными вложениями. Позволяет быстро предоставить описание компании, контактную информацию, услуги. Небольшой веб-ресурс, как правило до 5 страниц.",
    link: "#",
  },
  {
    title: "Интернет-магазин",
    text:
      "Онлайн-магазин с карточками товаров или услуг. Управление ценами и скидками прямо на сайте, онлайн-оплата с возможностью интеграции более 10 платежных систем или эквайринга. Интеграция с CRM-системами, онлайн-консультантом, виджетами, каталогом. Каталог с фильтрацией, категориями, поиском по ассортименту, возможностью импорта или экспорта продукции.",
    link: "#",
  },
];
</script>

<template>
  <section
    ref="sectionRef"
    class="bg-black text-white p-20 flex flex-row items-start relative gap-[250px] min-h-[200vh]"
  >
    <div class="w-[342px] h-[365px] shrink-0 sticky top-[80px]">
      <img
        :src="Diamond"
        alt="Crystal illustration"
        class="object-contain w-full h-full"
        style="transform: rotate(-3deg);"
      />
    </div>

    <div class="flex-1 ">
      <div class="content-block">
        <h2 class="heading-main">{{ mainContent.title }}</h2>
        <p class="text-gray-300 text-[24px]">{{ mainContent.text }}</p>
        <a :href="mainContent.link" class="link">
          Подробнее
          <img :src="RightArrow" alt="Arrow" class="arrow-icon" />
        </a>
        <hr class="h-[4px] bg-white" />
      </div>

      <div
        v-for="(item, index) in services"
        :key="index"
        class="content-block"
      >
        <h3 class="heading-sub">{{ item.title }}</h3>
        <p class="text-gray-300 text-[24px]">{{ item.text }}</p>
        <a :href="item.link" class="link">
          Подробнее
          <img :src="RightArrow" alt="Arrow" class="arrow-icon" />
        </a>
        <hr class="h-[4px] bg-white" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.content-block {
  margin-bottom: 55px;
}
.heading-main {
  font-size: 40px;
  font-weight: 600;
  margin-bottom: 25px;
}
.heading-sub {
  font-size: 36px;
  font-weight: 600;
  margin-bottom: 25px;
}
.content-block p {
  margin-bottom: 30px;
}
.link {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 55px;
  font-size: 24px;
  text-decoration: underline;
  text-underline-offset: 4px;
  color: #d1d5db;
  transition: color 0.3s ease;
}
.link:hover {
  color: #ffffff;
  text-decoration: none;
}
.arrow-icon {
  width: 28px;
  height: 28px;
  filter: invert(82%) sepia(6%) saturate(142%) hue-rotate(180deg) brightness(90%) contrast(90%);
  transform: scaleX(1.1);
}
.link:hover .arrow-icon {
  filter: invert(100%) brightness(100%);
}
</style>
