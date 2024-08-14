<script setup>
import { ref } from 'vue';
import CardVertical from './CardVertical.vue';
import Modal from './Modal.vue'
import { FreeMode, Pagination } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import 'swiper/css/free-mode';

const onSwiper = (swiper) => {
  console.log(swiper);
};

const onSlideChange = () => {
  console.log('slide change');
};
const modules = [FreeMode, Pagination];
// const slidesPerView = 1;
// const spaceBetween = ref(10);
const breakpoints = ref({
  '670': {
    slidesPerView: 2,
    spaceBetween: 5,
  },
  '950': {
    slidesPerView: 3,
    spaceBetween: 7,
  },
  '1240': {
    slidesPerView: 4,
    spaceBetween: 5,
  },
  '1740': {
    slidesPerView: 5.8,
    spaceBetween: 0,
  },
  '2240': {
    slidesPerView: 2,
    spaceBetween: 2,
  },
});
const showModal = ref(false)

function handleConfirm() {
  // Handle the confirm action
  showModal.value = false
}

const showLang = ref(false)
const showBranch = ref(false)
</script>

<template>
  <header class="">
    <img class="header_img" src="@/assets/images/header.jpg" alt="">
    <div class="">
      <div class="nav_menu border-b pb-2">
          <h2 class="text-black text-3xl font-bold tracking-wide">زاتشي</h2>
        <div class="flex flex-row-reverse items-center gap-6 ">
          <div class="flex items-center gap-2 font-Bahij font-bold px-3">
            إعدادات
            <svg version="1.1" class="bg-gray-900 text-white w-12 h-12 rounded-full p-2" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
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
          <div @click="showLang = !showLang" class="flex flex-row-reverse items-center hover:bg-[#ecf6fb] cursor-pointer"
                  id="menu-button" aria-expanded="true" aria-haspopup="true">
            <svg class="w-12 h-12 p-2 rounded-full bg-[#c2e8ef]" version="1.1" xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 256 256" enable-background="new 0 0 256 256"
              xml:space="preserve">
              <g>
                <g>
                  <path fill="#000000"
                    d="M243.1,138.3c-7.4-20.1-27.9-32.2-55-32.2c-1.1,0-2.1,0-3.1,0.1l-0.2-24.3c0,0,40.2-6.9,41.6-7.2s1.6-1.4,1.3-2.7c-0.3-1.3-2-10.4-2.2-11.5c-0.3-1.5-1.2-1.5-2.4-1.3s-38.3,5.4-38.3,5.4s-0.1-23-0.1-24.5c0-1.5-0.8-1.9-2.3-1.8c-1.5,0-10.9,0.2-12.1,0.2c-1.2,0-1.9,0.6-1.9,1.8c0,1.2,0.4,27.2,0.4,27.2s-36.1,6.2-37.1,6.4c-1,0.2-2,0.6-1.8,1.7s2.2,12.9,2.5,13.8c0.2,0.9,0.8,1.5,2.2,1.3c1.3-0.2,34.5-5.9,34.5-5.9l0.4,23.8c-12.7,3.3-21.2,9.7-26.6,15.4c-9.1,9.5-14.2,22.3-14.2,35c0,18.7,11.5,29.8,27.5,31.8c37.3,4.6,60.4-36.1,68.1-55.6c13,17.8,3,51.4-24.7,70.6c-0.5,0.3-1.2,1.5-0.4,2.4c0.8,0.9,6.4,7.8,7.3,8.9c0.9,1.1,2.4,0.7,3,0.3C238.8,196.8,252.4,163.9,243.1,138.3z M155.9,176c-11.4-1.4-11.1-10.8-11.1-17.1c0-9.1,3.9-18.6,10.3-25.4c3.9-4.2,8.8-7.3,14.5-9.4l1,50.5C166,176,161.2,176.6,155.9,176z M184.6,169.4l0.6-48.5c1,0,2-0.1,3-0.1c9.1,0,17.6,1.7,22.3,4.3C214.9,127.7,198.2,157.1,184.6,169.4z M78.9,79c-0.4-1.1-1.2-1.7-2.3-1.7h-23c-1.1,0-2,0.6-2.3,1.7c-4.9,15.3-41.1,129.7-41.3,130.3c-0.2,0.6-0.1,0.9,0.7,0.9h20.4c0.9,0,1.2-0.3,1.3-0.8c0.2-0.6,11.9-39.2,11.9-39.2h41.3c0,0,11.7,38.6,11.9,39.2c0.2,0.6,0.5,0.8,1.3,0.8h20.5c0.8,0,0.9-0.3,0.7-0.9C120,208.6,83.8,94.3,78.9,79z M48.1,153.5l17.1-61.9l17.1,61.9H48.1z" />
                </g>
              </g>
            </svg>
            <div class="relative inline-block text-right ">
              <div>
                <div
                  class="inline-flex flex-col w-full justify-center gap-x-1.5 rounded-md bg-white px-3 py-2  hover:bg-[#ecf6fb] cursor-pointer" >
                  <p class="text-lg font-Bahij font-bold">عربي</p>
                  <div class="flex flex-row-reverse items-end gap-2">
                    <p class="font-Bahij text-xs ">English</p>
                    <svg class="-mr-1 h-5 w-5 font-bold" viewBox="0 0 20 20" fill="black" aria-hidden="true">
                      <path fill-rule="evenodd"
                        d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
                        clip-rule="evenodd" />
                    </svg>
                  </div>
                </div>
              </div>
              <div v-if="showLang"
                class="absolute right-0 z-10 mt-2 w-32 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
                role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
                <div class="py-1" role="none">
                  <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
                  <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem" tabindex="-1" id="menu-item-0">English</a>
                  <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem" tabindex="-1"
                    id="menu-item-1">French</a>
                </div>
              </div>
            </div>
          </div>

          <div @click="showBranch = !showBranch" class="flex flex-row-reverse items-center hover:bg-[#ecf6fb] cursor-pointer"
            id="menu-button" aria-expanded="true" aria-haspopup="true">
            <div class="h-12 w-12 bg-[#c2e8ef] rounded-full"></div>
            <!-- <svg class="w-12 h-12 p-2 rounded-full bg-[#c2e8ef]" version="1.1" xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 256 256" enable-background="new 0 0 256 256"
              xml:space="preserve">
              <g>
                <g>
                  <path fill="#000000"
                    d="M243.1,138.3c-7.4-20.1-27.9-32.2-55-32.2c-1.1,0-2.1,0-3.1,0.1l-0.2-24.3c0,0,40.2-6.9,41.6-7.2s1.6-1.4,1.3-2.7c-0.3-1.3-2-10.4-2.2-11.5c-0.3-1.5-1.2-1.5-2.4-1.3s-38.3,5.4-38.3,5.4s-0.1-23-0.1-24.5c0-1.5-0.8-1.9-2.3-1.8c-1.5,0-10.9,0.2-12.1,0.2c-1.2,0-1.9,0.6-1.9,1.8c0,1.2,0.4,27.2,0.4,27.2s-36.1,6.2-37.1,6.4c-1,0.2-2,0.6-1.8,1.7s2.2,12.9,2.5,13.8c0.2,0.9,0.8,1.5,2.2,1.3c1.3-0.2,34.5-5.9,34.5-5.9l0.4,23.8c-12.7,3.3-21.2,9.7-26.6,15.4c-9.1,9.5-14.2,22.3-14.2,35c0,18.7,11.5,29.8,27.5,31.8c37.3,4.6,60.4-36.1,68.1-55.6c13,17.8,3,51.4-24.7,70.6c-0.5,0.3-1.2,1.5-0.4,2.4c0.8,0.9,6.4,7.8,7.3,8.9c0.9,1.1,2.4,0.7,3,0.3C238.8,196.8,252.4,163.9,243.1,138.3z M155.9,176c-11.4-1.4-11.1-10.8-11.1-17.1c0-9.1,3.9-18.6,10.3-25.4c3.9-4.2,8.8-7.3,14.5-9.4l1,50.5C166,176,161.2,176.6,155.9,176z M184.6,169.4l0.6-48.5c1,0,2-0.1,3-0.1c9.1,0,17.6,1.7,22.3,4.3C214.9,127.7,198.2,157.1,184.6,169.4z M78.9,79c-0.4-1.1-1.2-1.7-2.3-1.7h-23c-1.1,0-2,0.6-2.3,1.7c-4.9,15.3-41.1,129.7-41.3,130.3c-0.2,0.6-0.1,0.9,0.7,0.9h20.4c0.9,0,1.2-0.3,1.3-0.8c0.2-0.6,11.9-39.2,11.9-39.2h41.3c0,0,11.7,38.6,11.9,39.2c0.2,0.6,0.5,0.8,1.3,0.8h20.5c0.8,0,0.9-0.3,0.7-0.9C120,208.6,83.8,94.3,78.9,79z M48.1,153.5l17.1-61.9l17.1,61.9H48.1z" />
                </g>
              </g>
            </svg> -->
            <div class="relative inline-block text-right ">
              <div>
                <div
                  class="inline-flex flex-col w-full justify-center gap-x-1.5 rounded-md bg-white px-3 py-2  hover:bg-[#ecf6fb] cursor-pointer">
                  <p class="text-[15px] font-Bahij font-bold">فرع ام الفحم</p>
                  <div class="flex flex-row-reverse items-end gap-2">
                    <p class="flex flex-row-reverse gap-1 items-center font-Bahij text-xs p-0 m-0"><span class="h-3 w-3 bg-green-500 rounded-full p-1"></span>مفتوح الآن</p>
                    <svg class="-mr-1 h-5 w-5 font-bold" viewBox="0 0 20 20" fill="black" aria-hidden="true">
                      <path fill-rule="evenodd"
                        d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
                        clip-rule="evenodd" />
                    </svg>
                  </div>
                </div>
              </div>
              <div v-if="showBranch"
                class="absolute right-0 z-10 mt-2 w-32 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
                role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
                <div class="py-1" role="none">
                  <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
                  <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem" tabindex="-1" id="menu-item-0">القدس</a>
                  <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem" tabindex="-1"
                    id="menu-item-1">جنين</a>
                </div>
              </div>
            </div>
          </div>
          <div class="flex items-center justify-between gap-5 bg-[#50a6df] px-5 py-3 rounded-lg">
            <p class="text-white mr-4 text-[22px]">20 ₪</p>
            <div class="flex items-center gap-2">
              <p class="text-white text-[20px] font-bold">الطلبية</p>
              <span class="bg-white font-bold text-[20px] text-[#50a6df] px-[9px] rounded-full">5</span>
            </div>
          </div>
        </div>
      </div>
      
      <nav class="flex items-center justify-between py-4 px-9 shadow-xl shadow-gray-500/20">
        <div class="relative">
          <input type="text"
            class="w-full px-4 py-3 pr-8  rounded-full border-none bg-gray-100 border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500"
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

  <main class="md:px-12 md:py-4" dir="rtl">
    <div class="pt-4">
      <div class="pb-4" id="burger">
        <div class="flex items-center justify-between">
          <h2 class="text-[38px] font-bold text-black">برجر</h2>
          <a href="#" class="px-5 py-1 text-[#4da0db] bg-[#ecf6fb] rounded-full font-bold hover:bg-[#def4ff]">الكل</a>
        </div>
        <swiper :modules="modules" :freeMode="true"  @swiper="onSwiper" @slideChange="onSlideChange" :breakpoints="breakpoints">
          <swiper-slide>
            <div class="py-4 cursor-pointer" @click="showModal = true">
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

      <div class="py-4" id="salad">
        <div class="flex items-center justify-between">
          <h2 class="text-[38px] font-bold text-black">سلطات</h2>
          <a href="#" class="px-5 py-1 text-[#4da0db] bg-[#ecf6fb] rounded-full font-bold hover:bg-[#def4ff]">الكل</a>
        </div>
        <swiper :modules="modules" :space-between="spaceBetween"  @swiper="onSwiper" @slideChange="onSlideChange" :breakpoints="breakpoints">
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

    <div class="py-4" id="tortia">
      <div class="flex items-center justify-between">
        <h2 class="text-[38px] font-bold text-black">تورتيا</h2>
        <a href="#" class="px-5 py-1 text-[#4da0db] bg-[#ecf6fb] rounded-full font-bold hover:bg-[#def4ff]">الكل</a>
      </div>
        <swiper :modules="modules" :space-between="spaceBetween"  @swiper="onSwiper" @slideChange="onSlideChange" :breakpoints="breakpoints">
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
  <Modal :show="showModal" title="باجيت شوارما عجل"
    description="ميامي هو مشروب المشروب المحامي ميامي المشروب هو المشروب ميامي هو مشروب المشروب المحامي ميامي المشروب"
    @close="showModal = false" @confirm="handleConfirm" />

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