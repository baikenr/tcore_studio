<template>
    <section class="relative h-screen bg-cover bg-center bg-no-repeat text-white"
        :style="{ backgroundImage: `url(${bg_discussProject})` }">
        <div class="absolute inset-0 bg-black/60"></div>

        <div class="relative z-10 flex flex-col lg:flex-row">
            <div class="w-full flex flex-col px-10 lg:px-24 py-[7%]">
                <h2 class="text-gray-200 text-[48px] font-bold mb-4" style="font-weight: 700;">ОБСУДИТЬ ПРОЕКТ</h2>
                <p class="text-gray-200 text-[24px]">
                    Отправка заявки Вас ни к чему не обязывает.<br />
                    Созвонимся, проведём консультацию, <br />
                    финальное решение — за Вами.
                </p>
            </div>

            <div class="w-full flex justify-center pt-[8%] pr-[15%]">
                <div class="w-full rounded-4xl p-10 backdrop-blur" :style="{
                    backgroundImage: `url(${start_work_bg})`,
                    backgroundSize: 'cover',
                    backgroundPosition: 'center',
                    backgroundRepeat: 'no-repeat'
                }">
                    <h3 class="text-[40px] text-center pb-4">Начать работу</h3>
                    <p class="text text-center pb-18 text-[20px]">
                        Оставьте заявку и мы свяжемся с Вами в ближайшее время
                    </p>

                    <form class="space-y-5 flex flex-col items-center">
                        <div class="text-center pb-12 w-full">
                            <input type="text" placeholder="Как к Вам обращаться?"
                                class="w-[58%] bg-transparent border-b focus:border-white outline-none py-2 px-4 text-white text-[22px]" />
                        </div>

                        <div class="text-center pb-6 w-full">
                            <input type="tel" placeholder="Номер телефона для связи"
                                class="w-[58%] bg-transparent border-b focus:border-white outline-none py-2 px-4 text-white text-[22px]" />
                        </div>

                        <div class="flex items-center justify-center space-x-2 text-sm pb-14 w-full text-center">
                            <input type="checkbox" id="agree" class="custom-checkbox" />
                            <label for="agree" class="pl-4 text-left">
                                Нажимая кнопку “Зарегистрироваться”, вы соглашаетесь <br />на обработку ваших данных
                            </label>
                        </div>

                        <div class="relative w-[312px] h-[70px] mx-auto mb-8 group">
                            <img
                                :src="discuss_bottom"
                                alt="Зарегистрироваться"
                                class="absolute inset-0 w-full h-full object-cover cursor-pointer transition-transform duration-300 ease-out group-hover:brightness-110"
                                @click.prevent="submitForm"
                            />
                            <span
                                class="absolute inset-0 flex items-center justify-center text-white font-bold text-[24px] pointer-events-none transition-colors duration-300 group-hover:text-[#BE9F56]"
                            >
                                Зарегистрироваться
                            </span>
                            </div>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import bg_discussProject from '@/assets/images/bg_discussProject.png'
import discuss_bottom from '@/assets/images/discuss_bottom.svg'
import start_work_bg from '@/assets/images/start_work_bg.svg'
</script>

<style scoped>
.custom-checkbox {
    width: 28px;
    height: 28px;
    border: 3px solid #fff;
    background: transparent;
    appearance: none;
    cursor: pointer;
    position: relative;
    transition: all 0.2s ease;
}

.custom-checkbox:checked {
    background-color: #be9f56;
    border-color: #be9f56;
}

.custom-checkbox:checked::after {
    content: "";
    position: absolute;
    left: 7px;
    top: 2px;
    width: 8px;
    height: 16px;
    border-right: 3px solid white;
    border-bottom: 3px solid white;
    transform: rotate(45deg);
}
</style>
