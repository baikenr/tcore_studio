<template>
  <section
    class="relative w-full min-h-screen overflow-hidden text-white"
    aria-label="Наши проекты"
    style="font-family:'Manrope',sans-serif; background:linear-gradient(180deg,#09101a 0%,#0b0b0c 100%)"
  >
    <img
      src="@/assets/images/bg_pg2.png"
      alt="Фон страницы проектов"
      class="absolute inset-0 w-full h-full object-cover object-center opacity-60 z-[1]"
    />
    <div class="relative z-[2] px-[8vw] pt-[6vh]">
      <h2
        class="font-bold text-[clamp(26px,1.6vw,32px)] leading-[145%] tracking-[0.02em] mb-[4vh]"
      >
        Наши проекты
      </h2>
      <div
        class="relative w-[55vw] h-[28vw] border-[0.3vw] border-black rounded-[0.3vw] overflow-hidden mb-[5vh]"
      >
        <img
          src="@/assets/images/mockup.png"
          alt="Превью проекта"
          class="w-full h-full object-cover"
        />
        <div class="absolute bottom-[2.5vh] right-[3vw] text-right">
          <button
            class="text-[clamp(16px,1vw,19px)] font-medium leading-[145%] tracking-[0.02em] hover:opacity-80 transition"
          >
            Подробнее о проекте
          </button>
          <div class="w-[10vw] h-[0.25vh] bg-white/90 mt-[0.5vh] ml-auto"></div>
        </div>
      </div>
      <div
        class="absolute top-[15vh] right-[10vw] flex flex-col gap-[2.5vh] text-[clamp(18px,1.3vw,25px)] font-normal leading-[140%] tracking-[0.02em]"
      >
        <div class="relative">
          <p>
            Лендинги<sup class="ml-[0.3vw] text-[clamp(12px,0.8vw,14px)] opacity-80">3</sup>
          </p>
          <div class="absolute top-[115%] left-0 w-[6vw] h-[0.3vh] bg-white/90 rounded-[11px]"></div>
        </div>
        <p>
          E-com проекты<sup class="ml-[0.3vw] text-[clamp(12px,0.8vw,14px)] opacity-80">8</sup>
        </p>
        <p>
          CRM-системы<sup class="ml-[0.3vw] text-[clamp(12px,0.8vw,14px)] opacity-80">4</sup>
        </p>
      </div>

      <h3
        class="text-[clamp(20px,1.3vw,24px)] font-bold w-[35vw] mt-[6vh] mb-[2vh]"
      >
        Разбираемся за неделю даже в сложной нише
      </h3>

      <p
        class="text-[clamp(16px,1.1vw,20px)] font-light text-white/90 w-[55vw] leading-[145%] mb-[4vh]"
      >
        Сайты нашего дизайн-агентства привлекают клиентов и увеличивают продажи в инженерии,
        инфобизнесе, косметологии или ковшах для экскаваторов :)
      </p>

      <h4
        class="text-[clamp(20px,1.2vw,25px)] font-extrabold leading-[145%] mb-[1vh]"
      >
        О проекте:
      </h4>

      <p
        class="text-[clamp(16px,1.1vw,20px)] font-light text-white/90 w-[55vw] leading-[145%]"
      >
        Главная идея: Передать ощущение свежести, прозрачности и прямого контакта с производителем.
        Интерфейс — простой и интуитивный, как рынок под открытым небом, но в цифре.
      </p>
    </div>
  </section>
</template>
