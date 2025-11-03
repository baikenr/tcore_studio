<template>
  <section class="support" aria-label="Персональная поддержка">
    <img class="bg" src="@/assets/images/sand.png" alt="" />
    <h2 class="title">
      Персональная. В любое время.<br />
      Лучшая <strong>поддержка</strong> здесь
    </h2>

    <p class="lead">
      Откройте для себя индивидуальную поддержку и сопровождение на вашем пути с помощью нашего
      приложения для помощи в выборе, где наша поддержка предоставляет вам лучший выбор для вашего сайта
    </p>
    <div class="bubble bubble--ru">
      Здравствуйте! Вы сегодня свободны?
    </div>

    <div class="bubble bubble--en1">
      I've been feeling really overwhelmed lately. <br />
      I have a lot of work piling up, and I'm <br />
      struggling to manage my time effectively.
    </div>

    <div class="bubble bubble--en2">
      I understand how overwhelming that can be.<br />
      It's important to address this issue step by<br />
      step. Let's start by identifying your priorities.<br />
      What are the most important tasks on your<br />
      to-do list?
    </div>
    <div class="num num--users">200K</div>
    <div class="cap cap--users">
      A worldwide user<br />
      every month
    </div>

    <div class="num num--ok">85%</div>
    <div class="cap cap--ok">
      Successfully solved<br />
      problems
    </div>
  </section>
</template>

<style scoped>
.support {
  position: relative;
  width: 100%;
  height: 1057px;
  overflow: hidden;
  color: #fff;
  font-family: "Manrope", sans-serif;
  background: rgba(4, 6, 17, 1);
}

.bg {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: 50% 40%;
  filter: brightness(0.85);
  z-index: 1;
}

.title {
  position: absolute;
  top: 100px;
  left: 98px;
  width: 950px;
  height: 188px;
  font-weight: 400;
  font-size: clamp(62px, 2.9vw, 75px);
  line-height: 145%;
  letter-spacing: 0.02em;
  margin: 0;
  z-index: 2;
}
.title strong {
  font-weight: 800;
}

.lead {
  position: absolute;
  top: 405px;
  left: 98px;
  width: 962px;
  height: 260px;
  font-weight: 400;
  font-size: clamp(28px, 1.875vw, 36px);
  line-height: 145%;
  letter-spacing: 0.02em;
  color: rgba(255, 255, 255, 0.92);
  z-index: 2;
}

.bubble {
  position: absolute;
  width: 637px;
  color: #000;
  font-size: clamp(22px, 1.46vw, 28px); line-height:145%; letter-spacing:.02em;
  line-height: 145%;
  letter-spacing: 0.02em;
  /* padding: 24px 32px; */
  z-index: 2;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.25);
}

.bubble--ru {
  padding: 22px 24px 20px 28px; 
  top: 167px;
  left: 1120px;
  height: 136px;
  background: rgba(253, 253, 253, 0.6);
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
  color:rgba(255, 255, 255, 1);
}

.bubble--en1 {
  padding: 18px 26px 18px 28px;
  top: 356px;
  left: 1181px;
  height: 170px;
  background: rgba(253, 253, 253, 1);
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  border-bottom-left-radius: 20px;
}

.bubble--en2 {
  padding: 16px 24px 22px 22px;
  top: 601px;
  left: 1120px;
  height: 280px;
  background: rgba(253, 253, 253, 0.6);
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
  color:rgba(255, 255, 255, 1);
}

.num {
  position: absolute;
  font-weight: 800;
  font-size: 80px;
  line-height: 145%;
  letter-spacing: 0.02em;
  z-index: 2;
}
.cap {
  position: absolute;
  font-weight: 500;
  font-size: 20px;
  line-height: 145%;
  letter-spacing: 0.02em;
  color: rgba(255, 255, 255, 0.85);
  z-index: 2;
}

.num--users {
  top: 886px;
  left: 98px;
}
.cap--users {
  top: 913px;
  left: 335px;
}

.num--ok {
  top: 886px;
  left: 601px;
}
.cap--ok {
  top: 913px;
  left: 796px;
}
</style>
