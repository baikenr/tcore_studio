<script setup>
const footerBlocks = [
  { title: "Текст", texts: ["Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст"] },
  { title: "Текст", texts: ["Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст"] },
  { title: "Текст", texts: ["Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст"] },
  { title: "Текст", texts: ["Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст","Текст текст текст текст"] },
];
</script>

<template>
  <footer class="footer-section relative text-gray-300 flex items-center py-12 h-[416px] justify-center">
    <div class="absolute inset-0 bg-[#21212D]/95 z-[1]"></div>

    <div class="relative z-[2] mx-auto px-8 w-full max-w-[1600px] ">
      <div class="flex flex-col md:flex-row items-start gap-16 text-center md:text-left">

        <div class="md:w-[30%] max-w-[380px]">
          <h4 class="text-white text-[24px] mb-4 font-bold">Немного про нас</h4>
          <p class="text-gray-300 text-[16px] leading-relaxed">
            Хотим, чтобы ваш сайт был не очередным шаблоном,
            <br />а конверсионным, продающим,
            <br />запоминающимся и работал
            <br />в том числе на нашу репутацию.
          </p>
        </div>

        <div class="hidden md:flex items-center justify-center px-6">
          <span class="w-[3px] h-[180px] bg-white/80 rounded-full"></span>
        </div>

        <div class="flex-1">
          <div class="grid grid-cols-2 lg:grid-cols-4 gap-x-14">
            <div
              v-for="(block, index) in footerBlocks"
              :key="index"
              class="text-[16px] leading-relaxed"
            >
              <h5 class="text-white text-[18px] font-semibold text-center block mb-4">
                {{ block.title }}
              </h5>

              <div class="space-y-1 pt-2">
                <p v-for="(text, i) in block.texts" :key="i">
                  {{ text }}
                </p>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer-section {
  background-image: url('@/assets/images/bg_footer.png');
  background-size: cover;
  background-position: center;
  position: relative;
}
</style>
