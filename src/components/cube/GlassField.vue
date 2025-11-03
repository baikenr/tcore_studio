<template>
  <div class="w-full flex justify-center"
       style="--s:min(1,calc(200vw/1920)); transform:scale(var(--s)); transform-origin:top center;">
    <div class="relative w-full max-w-[1349px] h-[356px] mx-auto rounded-[10px] border-[2px] overflow-hidden"
         :style="glassBorderStyle">

      <div class="absolute inset-0 bg-[rgba(0,0,0,0.4)] backdrop-blur-[50px]"></div>

      <div class="absolute h-[2px] bg-white/30"
           style="left:var(--padX); right:var(--padX); top:var(--railTop);">

        <div class="absolute -top-[11px] size-[18px] rounded-full bg-white shadow"
             style="left:0;"></div>

        <div class="absolute -top-[6px] size-[10px] rounded-full bg-white"
             style="left:calc(var(--p2) * (100%));"></div>

        <div class="absolute -top-[6px] size-[10px] rounded-full bg-white"
             style="left:calc(var(--p3) * (100%));"></div>

        <div class="absolute -top-[6px] size-[10px] rounded-full bg-white"
             style="left:calc(var(--p4) * (100%));"></div>

        <div class="absolute -top-[6px] size-[10px] rounded-full bg-white"
             style="right:0;"></div>
      </div>

      <div class="absolute text-white text-[14px]"
           style="left:calc(var(--padX)); top:calc(var(--railTop) + 16px);">
        Вы тут
      </div>

      <div
        class="absolute border-[3px] border-white/45 rounded-full"
        style="
            left: 50%;
            transform: translateX(-50%);
            bottom: var(--circleBottom);
            width: var(--circleSize);
            height: var(--circleSize);
        "
        ></div>


      <div class="absolute text-center leading-tight"
           style="left:50%; transform:translateX(-50%); bottom:var(--titleBottom);">
        <div class="text-white font-semibold text-[20px]">Часть 1. Вы</div>
        <div class="text-white/85 text-[20px]">It Starts with You</div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

const glassBorderStyle = {
  borderImageSlice: 1,
  borderImageSource:
    'radial-gradient(86.82% 86.82% at 50% 0.91%, #FFFFFF 0%, rgba(255,255,255,0) 100%), radial-gradient(50% 50% at 50% 100%, #FFFFFF 0%, rgba(255,255,255,0.03) 100%)'
}
</script>

<style scoped>
:host, .w-full {
  --padX: 88px;
  --railTop: 82px; 
  --p2: 0.25; 
  --p3: 0.50;
  --p4: 0.75;

  --circleSize: 833px;
  --circleBottom: -667px;
  --titleBottom: 82px;
}
</style>
