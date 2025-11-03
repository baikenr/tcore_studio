<template>
  <div class="bubbles" aria-hidden="true">
    <div class="bubble bubble--small-ru">Здравствуйте! Вы сегодня свободны?</div>

    <div class="bubble bubble--en-1">
      I've been feeling really overwhelmed lately.
      I have a lot of work piling up, and I'm
      struggling to manage my time effectively.
    </div>

    <div class="bubble bubble--en-2">
      I understand how overwhelming that can be.
      It's important to address this issue step by step.
      Let's start by identifying your priorities.
      What are the most important tasks on your to-do list?
    </div>
  </div>
</template>

<style scoped>
.bubbles{
  position: absolute;
  top: 90px;
  left: 720px;
  width: 820px;
  pointer-events: none;
}

.bubble{
  display: inline-block;
  max-width: 760px;
  padding: 18px 22px;
  margin: 0;
  border-radius: 12px;
  background: rgba(255,255,255,.18);
  color: #000;
  font-size: 16px;
  line-height: 145%;
  letter-spacing: 0.01em;
  backdrop-filter: blur(3px);
  color: #e9e9e9;
  box-shadow: 0 2px 8px rgba(0,0,0,.25);
}

.bubble--small-ru{
  position: absolute;
  top: 20px; left: 0;
  padding: 14px 18px;
  font-size: 15px;
  background: rgba(255,255,255,.22);
}

.bubble--en-1{
  position: absolute;
  top: 130px; left: 60px;
  width: 520px;
}

.bubble--en-2{
  position: absolute;
  top: 290px; left: 20px;
  width: 610px;
}
</style>
