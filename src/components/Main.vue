<script setup>
import { ref } from 'vue';
import CardVertical from './CardVertical.vue';
import { Pagination } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';

const onSwiper = (swiper) => {
  console.log(swiper);
};

const onSlideChange = () => {
  console.log('slide change');
};
const modules = [Pagination];
const slidesPerView = 1;
const spaceBetween = ref(10);
const breakpoints = ref({
  '670': {
    slidesPerView: 2,
    spaceBetween: 20,
  },
  '950': {
    slidesPerView: 3,
    spaceBetween: 10,
  },
  '1240': {
    slidesPerView: 4,
    spaceBetween: 15,
  },
  '1740': {
    slidesPerView: 5,
    spaceBetween: 15,
  },
  '2140': {
    slidesPerView: 6,
    spaceBetween: 15,
  },
});
</script>

<template>
  <header class="relative">
    <img class="header_img" src="@/assets/images/header.jpg" alt="">
    <div class="sticky w-full bottom-0 z-40">
      <div class="nav_menu border-b">
        <h2 class="text-gray-700 text-3xl font-bold tracking-wider">زاتشي</h2>
        <div class="flex flex-row-reverse items-center gap-4">
          <div class="flex items-center gap-1">
            إعدادات
            <svg version="1.1" class="bg-gray-900 text-white rounded-full p-1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
              viewBox="0 0 256 256" width="28" height="28" enable-background="new 0 0 256 256" xml:space="preserve">
              <g>
                <g>
                  <g>
                    <path fill="#fff"
                      d="M116.4,11.3c-4.3,2.2-4.8,3.5-7.3,18.1L107,41.9l-6.5,2.2c-7.1,2.4-11.2,4.1-15.5,6.7c-1.5,0.9-3,1.5-3.3,1.3c-0.3-0.2-4.8-3.4-10.1-7.1c-5.2-3.7-10.1-7.1-10.8-7.3c-2.2-0.8-5.9-0.6-8.1,0.5c-2.6,1.2-13.9,12.6-14.9,15c-0.9,2-1,5.9-0.3,7.8c0.3,0.7,3.6,5.7,7.5,11.1c3.8,5.4,7,10,7,10.2c0,0.2-1.5,3.5-3.3,7.1c-1.8,3.7-4.1,9.1-5,12.1c-1.4,4.4-1.9,5.4-2.7,5.6c-0.6,0.1-6,1.1-12.2,2.1c-6.1,1-11.9,2.2-12.9,2.6c-2.4,1-3.7,2.4-5,5c-1,2.2-1.1,2.8-1.1,11.3c0,8.5,0.1,9.1,1.1,11.3c1.2,2.7,2.6,4.1,5,5c0.9,0.4,6.7,1.6,12.9,2.6c6.2,1,11.7,1.9,12.2,2.1c0.8,0.2,1.3,1.2,2.7,5.6c0.9,3,2.7,7.7,3.9,10.4l2.2,4.9l-7.6,9.4c-4.2,5.1-8,10.2-8.4,11.2c-1.2,2.5-1.1,6.2,0.1,8.6c1.4,2.8,11.7,14.1,13.7,15.1c5,2.5,6.6,2,19.7-6.2l10.8-6.8l4.3,2.6c6,3.6,11.4,6,18.5,8.3l6,1.9l2.1,12.4c1.2,6.8,2.3,12.8,2.5,13.3c0.8,2,2.7,3.9,5,5.1c2.3,1.1,2.6,1.2,11.1,1.2c4.8,0,9.5-0.2,10.5-0.5c2.1-0.6,5.2-3.2,6.2-5.3c0.4-0.9,1.7-7.2,2.8-14c1.2-6.7,2.1-12.3,2.2-12.3c0,0,2.8-0.9,6.2-2c3.5-1.1,8.7-3.3,12.2-5.1l6.1-3.1l10.4,7.4c5.8,4.1,11.2,7.7,11.9,8c2.3,0.8,5.5,0.6,7.6-0.4c2.4-1.2,14.2-13.1,15.2-15.3c0.9-2.1,0.9-5.4,0-7.6c-0.4-0.9-3.9-6.2-7.8-11.7c-3.9-5.5-7.1-10.2-7.1-10.4c0-0.2,1.2-2.8,2.7-5.7c2.8-5.5,5.5-12.3,6.5-16.5c0.5-1.8,0.8-2.5,1.5-2.6c0.6-0.1,6-1.1,12.1-2.1c6.1-1,11.7-2.1,12.4-2.4c2.3-0.9,4.4-2.8,5.5-5.2c1.1-2.2,1.1-2.9,1.1-11.3c0-8.5-0.1-9.1-1.1-11.3c-1.2-2.5-3-4.3-5.2-5.2c-0.7-0.3-6.4-1.4-12.6-2.4s-11.7-1.9-12.2-2.1c-0.7-0.1-1.2-1.2-2.2-4.7c-0.7-2.5-2.4-7-3.6-10l-2.3-5.4l7.4-9.2c9.3-11.5,9.5-11.8,9.5-15.7c0-3.9-0.7-5.1-7.8-12.9c-3.8-4.2-6-6.4-7.4-7c-2.3-1-5.7-1.1-7.8-0.2c-0.8,0.4-6,3.5-11.5,6.9c-5.5,3.5-10.1,6.3-10.2,6.3c-0.2,0-2-1-4.1-2.3c-6.1-3.7-13-6.9-19.4-8.9c-3.3-1.1-6-1.9-6.1-2c0,0-1-5.6-2.2-12.3c-1.1-6.8-2.4-13-2.8-14c-1-2.1-4.1-4.7-6.2-5.3c-0.9-0.2-5.6-0.5-10.5-0.5C119,10,118.9,10,116.4,11.3z M139.3,85.1c21.3,5.6,35.6,26.3,33,47.9c-2.3,18.4-15.2,33.2-33.2,38c-5.1,1.3-15.5,1.5-20.4,0.2c-13.7-3.4-24.8-12.5-30.6-24.9c-2.9-6.1-3.7-10.2-3.7-18.3c0-6,0.2-7.7,1.1-11c4-14.8,15.1-26.4,29.5-31.2C122.1,83.5,132.2,83.2,139.3,85.1z" />
                  </g>
                </g>
              </g>
            </svg>
          </div>
          <div class="flex items-center gap-1">
            عربي
            <svg version="1.1" class=" text-white rounded-full" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
              viewBox="0 0 256 256" width="28" height="28" enable-background="new 0 0 256 256" xml:space="preserve">
              <g>
                <path fill="#000"
                  d="M166.4,77.8c4.4,13.3,10.3,23.6,20.7,34c8.9-8.9,14.8-20.7,19.2-34H166.4z M69,151.6h38.4L88.2,99.9 L69,151.6z" />
                <path fill="#000"
                  d="M216.5,9.9h-177C23.3,9.9,10,23.2,10,39.4v177.2c0,16.2,13.3,29.5,29.5,29.5h177 c16.2,0,29.5-13.3,29.5-29.5V39.4C246,23.2,234.2,9.9,216.5,9.9L216.5,9.9z M144.2,200.3c-2.9,3-5.9,3-8.8,3c-1.5,0-4.4,0-5.9-1.5 c-1.5-1.5-3,0-3-1.5s-1.5-3-2.9-5.9c-1.5-3-1.5-4.4-3-7.4l-5.9-16.2H63.1l-5.9,16.2c-2.9,5.9-4.4,10.3-5.9,13.3c-1.5,3-4.4,3-8.8,3 c-3,0-5.9-1.5-8.9-3c-2.9-3-4.4-4.4-4.4-7.4c0-1.5,0-3,1.5-5.9c1.5-3,1.5-4.4,2.9-7.4L66,97c1.5-3,1.5-5.9,3-8.9 c1.5-3,2.9-5.9,4.4-7.4c1.5-1.5,3-4.4,5.9-5.9c3-1.5,5.9-1.5,8.9-1.5c2.9,0,5.9,0,8.8,1.5c2.9,1.5,4.4,3,5.9,5.9 c1.5,1.5,2.9,4.4,4.4,7.4c1.5,3,3,5.9,4.4,10.3l32.4,81.2c3,5.9,4.4,10.3,4.4,13.3C147.2,194.4,145.7,197.4,144.2,200.3z  M225.4,142.8c-16.2-5.9-28-13.3-38.4-22.1c-10.3,10.3-23.6,17.7-39.8,22.1l-4.4-7.4c16.2-4.4,29.5-10.3,39.8-20.7 c-10.3-10.3-19.2-23.6-22.1-38.4h-14.7v-5.9h39.8c-3-4.4-5.9-10.3-8.9-14.8l4.4-1.5c3,4.4,7.4,10.3,10.3,16.2h36.9v7.4h-14.8 c-4.4,14.8-11.8,28.1-20.6,36.9c10.3,8.9,22.1,16.2,38.4,20.7L225.4,142.8L225.4,142.8z" />
              </g>
            </svg>
          </div>
          <div class="flex items-center gap-1">
            فرع ام الفحم
            <svg version="1.1" class=" text-white rounded-full" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
              viewBox="0 0 256 256" width="28" height="28" enable-background="new 0 0 256 256" xml:space="preserve">
              <g>
                <g>
                  <path fill="#000000"
                    d="M227.5,10h-199C18.3,10,10,18.3,10,28.5v199c0,10.2,8.3,18.5,18.5,18.5h199c10.2,0,18.5-8.3,18.5-18.5v-199C246,18.3,237.7,10,227.5,10z M195.4,79.2h-0.5l0-0.2L195.4,79.2z M69.9,56h116.2c3.9,0,7,2.8,7,6.3c0,3.5-3.1,6.3-7,6.3H69.9c-3.8,0-7-2.8-7-6.3C63,58.8,66.1,56,69.9,56z M195.4,191.7c0,3.7-4.7,8.4-8.9,8.4H69.6c-4.2,0-8.9-4.7-8.9-8.4v-43.9h11.6l0,0v41.8h111.5v-41.8c0,0,1.6,0,2.3,0h9.3V191.7L195.4,191.7z M189,135.5c-11.2,0-20.3-8.9-20.3-19.9c0,11-9.1,19.9-20.3,19.9c-11.2,0-20.3-8.9-20.3-19.9c0,11-9.1,19.9-20.3,19.9s-20.3-8.9-20.3-19.9c0,11-9.1,19.9-20.3,19.9s-20.3-8.9-20.3-19.9l13.9-36.4h134.3l14.5,36.4C209.3,126.6,200.2,135.5,189,135.5z" />
                </g>
              </g>
            </svg>
          </div>
          <div class="flex items-center justify-between gap-5 bg-[#50a6df] p-5 rounded-2xl">
            <p class="text-white">20 ₪</p>
            <div class="flex items-center gap-2">
              <p class="text-white">الطلبية</p>
              <span class="bg-white text-[#50a6df] px-2 rounded-full">5</span>
            </div>
          </div>
        </div>
      </div>
      
      <nav class="flex items-center justify-between py-4 px-9 shadow-xl shadow-gray-500/20">
        <div class="relative">
          <input type="text"
            class="w-full px-4 py-2 pr-8 rounded-full border-none bg-gray-100 border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500"
            placeholder="بحث..."  dir="rtl"/>
          <div class="absolute inset-y-0 right-0 flex items-center pr-3">
            <svg class="h-5 w-5 text-gray-400 -mx-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
            </svg>
          </div>
        </div>
        <div class="flex flex-row-reverse items-center gap-3 text-lg ">
          <a href="#burger" class="px-3 py-2 font-semibold text-gray-800 hover:text-[#439BD9]">برجر</a>
          <a href="#salad" class="px-3 py-2 font-semibold text-gray-800 hover:text-[#439BD9]">سلطات</a>
          <a href="#tortia" class="px-3 py-2 font-semibold text-gray-800 hover:text-[#439BD9]">تورتيا</a>
          <a href="# " class="px-3 py-2 font-semibold text-gray-800 hover:text-[#439BD9]">تورتيا</a>
          <a href="#" class="px-3 py-2 font-semibold text-gray-800 hover:text-[#439BD9]">إضافات</a>
          <a href="#" class="px-3 py-2 font-semibold text-gray-800 hover:text-[#439BD9]">مشروبات</a>
        </div>
      </nav>
    </div>
  </header>

  <main class="px-12 py-4" dir="rtl">
    <div class="pt-6">
      <div class="py-2" id="burger">
        <h2 class="text-2xl font-bold text-gray-800">برجر</h2>
        <swiper :modules="modules" :space-between="spaceBetween" :pagination="{
          clickable: true}" @swiper="onSwiper" @slideChange="onSlideChange" :breakpoints="breakpoints">
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
        </swiper>
      </div>

      <div class="py-2" id="salad">
        <h2 class="text-2xl font-bold text-gray-800">سلطات</h2>
        <swiper :modules="modules" :space-between="spaceBetween" :pagination="{
          clickable: true}" @swiper="onSwiper" @slideChange="onSlideChange" :breakpoints="breakpoints">
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </div>

    <div class="py-2" id="tortia">
      <h2 class="text-2xl font-bold text-gray-800">ترتيا</h2>
        <swiper :modules="modules" :space-between="spaceBetween" :pagination="{
          clickable: true
        }" @swiper="onSwiper" @slideChange="onSlideChange" :breakpoints="breakpoints">
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="py-4">
              <CardVertical />
            </div>
          </swiper-slide>
        </swiper>
      </div>
  </main>

</template>

<style scoped>
.header_img {
  width: 100vw;
  height: 25rem;
  object-fit: cover;
}

.nav_menu {
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
  justify-content: space-between;
  padding: 8px 3rem
}
</style>