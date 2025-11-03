<template>
  <div class="w-full flex justify-center"
       style="--s:min(1,calc(200vw/1920));transform:scale(var(--s));transform-origin:top center;">
    <div
      class="relative mx-auto w-[1085px] h-[400px] rounded-[10px] border-[2px] overflow-hidden"
      :style="glassBorderStyle"
    >
      <div class="pointer-events-none absolute inset-0">
        <div class="absolute inset-0 bg-black/40 backdrop-blur-[50px]"></div>
        <div
          class="absolute -left-1/3 -top-1/3 w-[140%] h-[140%] opacity-20 rounded-full
                 [background:radial-gradient(60%_60%_at_50%_0%,_#fff,_rgba(255,255,255,0))]">
        </div>
        <div
          class="absolute -right-1/3 -bottom-1/2 w-[120%] h-[120%] opacity-5 rounded-full
                 [background:radial-gradient(50%_50%_at_50%_100%,_#fff,_rgba(255,255,255,0))]">
        </div>
      </div>

      <div class="relative z-[1] text-white px-8 py-7">
        <p class="font-medium text-[20px] leading-[145%] tracking-[0.02em] text-white/90">
          Lorem ipsum dolor sit amet consectetur adipiscing elit. Quisque faucibus ex sapien vitae
          pellentesque sem placerat. In id cursus mi pretium tellus duis convallis. Tempus leo eu aenean
          sed diam urna tempor. Pulvinar vivamus fringilla lacus nec metus bibendum egestas. Iaculis
          massa nisl malesuada lacinia integer nunc posuere. Ut hendrerit semper vel class aptent taciti
          sociosqu. Ad litora torquent per conubia nostra inceptos himenaeos.
        </p>
        <div class="h-[20px]"></div>
        <p class="mt-6 font-medium text-[20px] leading-[145%] tracking-[0.02em] text-white/90">
          Lorem ipsum dolor sit amet consectetur adipiscing elit. Quisque faucibus ex sapien vitae
          pellentesque sem placerat. In id cursus mi pretium tellus duis convallis. Tempus leo eu aenean
          sed diam urna tempor. Pulvinar vivamus fringilla lacus nec metus bibendum egestas. Iaculis massa
          nisl malesuada lacinia integer nunc posuere. Ut hendrerit semper vel class aptent taciti sociosqu.
          Ad litora torquent per conubia nostra inceptos himenaeos.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const glassBorderStyle = {
  borderImageSlice: 1,
  borderImageSource:
    'radial-gradient(86.82% 86.82% at 50% 0.91%, #FFFFFF 0%, rgba(255,255,255,0) 100%), ' +
    'radial-gradient(50% 50% at 50% 100%, #FFFFFF 0%, rgba(255,255,255,0.03) 100%)'
}
</script>
