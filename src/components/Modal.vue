<script setup>
defineProps({
  show: {
    type: Boolean,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
})

defineEmits(['close', 'confirm'])

</script>

<template>
  <div class="fixed z-10 inset-0 overflow-y-auto" v-if="show">
    <div class="flex items-end justify-center min-h-screen pt-4 px-4 pb-20 text-center sm:block sm:p-0">
      <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" aria-hidden="true"></div>
  
      <span class="hidden sm:inline-block sm:align-middle sm:h-screen" aria-hidden="true">&#8203;</span>
  
      <div
        class="relative inline-block align-bottom bg-white rounded-lg text-left overflow-hidden shadow-xl transform transition-all sm:my-8 sm:align-middle sm:max-w-lg sm:w-full">
        <div class="bg-white pb-4 sm:pb-4">
          <div class="">
            <div
              class="w-full mb-4">
              <img src="@/assets/images/burger.jpg" alt="Sandwich image" class="h-auto w-full object-cover" />
            </div>
            
            <div class="p-6 text-right">
              <div class="flex flex-row-reverse items-center justify-between pb-3">
                <h3 class="text-2xl leading-6 font-medium text-black">{{ title }}</h3>
                <p class="text-2xl font-bold">₪25 <span class="text-gray-400 line-through mx-2">₪45</span></p>
              </div>
              <div class="mt-2">
                <p class="text-lg font-medium text-black">{{ description }}</p>
              </div>
            </div>
            <div class="flex flex-row-reverse items-center justify-center gap-4">
              <div class="flex flex-col items-center justify-center p-4 bg-black rounded-full text-white w-16 h-16">
                <p class="font-Bahij text-lg font-bold">كامل</p>
                <p class="font-Bahij text-lg font-bold">₪45</p>
              </div>
              <div class="flex flex-col items-center justify-center p-4 border-2 border-black rounded-full text-black w-16 h-16">
                <p class="font-Bahij text-lg font-bold">نُص</p>
                <p class="font-Bahij text-lg font-bold">₪28</p>
              </div>
            </div>
          </div>
        </div>
        
        <div class="relative p-6" dir="rtl">
          <table class="table-fixed w-full rounded-lg border-tools-table-outline ">
            <thead class="p-4 ">
              <tr class="bg-[#f7efea] p-4">
                <th class="text-right px-4 py-3 font-bold rounded-tr-xl rounded-br-xl">سَلطات</th>
                <th class="text-left px-4 py-3 font-bold rounded-tl-xl rounded-bl-xl">مجاناً</th>
              </tr>
            </thead>
            <tbody class="text-xs font-Bahij">
              <tr>
                <td class="flex items-center justify-start gap-2 px-3 py-1">
                  <input type="checkbox" class="form-checkbox h-5 w-5 text-orange-500" />
                  <img src="@/assets/images/humos.png" alt="Checkbox" class="h-6 w-6" />
                  <p>حمص</p>
                </td>
                <td class="px-4 py-1 text-gray-400">$10</td>
              </tr>
              <tr>
                <td class="flex  items-center justify-start gap-2 px-3 py-1">
                  <input type="checkbox" class="form-checkbox h-5 w-5 text-orange-500" />
                  <img src="@/assets/images/humos.png" alt="Checkbox" class="h-6 w-6" />
                  <p>طحينة</p>
                </td>
                <td class="px-4 py-1 text-gray-400">$10</td>
              </tr>
              <tr>
                <td class="flex  items-center justify-start gap-2 px-3 py-1">
                  <input type="checkbox" class="form-checkbox h-5 w-5 text-orange-500" />
                  <img src="@/assets/images/humos.png" alt="Checkbox" class="h-6 w-6" />
                  <p>سلط تركي</p>
                </td>
                <td class="px-4 py-1 text-gray-400">$10</td>
              </tr>
              <tr>
                <td class="flex  items-center justify-start gap-2 px-3 py-1">
                  <input type="checkbox" class="form-checkbox h-5 w-5 text-orange-500" />
                  <img src="@/assets/images/humos.png" alt="Checkbox" class="h-6 w-6" />
                  <p>ذرة</p>
                </td>
                <td class="px-4 py-1 text-gray-400">$10</td>
              </tr>
              <tr>
                <td class="flex  items-center justify-start gap-2 px-3 py-1">
                  <input type="checkbox" class="form-checkbox h-5 w-5 text-orange-500" />
                  <img src="@/assets/images/humos.png" alt="Checkbox" class="h-6 w-6" />
                  <p>سلطة عربية</p>
                </td>
                <td class="px-4 py-1 text-gray-400">$10</td>
              </tr>
              <!-- Add more rows as needed -->
            </tbody>
          </table>
          <div class=" absolute bottom-6 flex w-full gap-2">
            <div class="flex items-center gap-5 px-2 py-4 bg-[#ffe2d0] rounded-lg basis-1/4">
              <svg class="w-7 h-7 bg-[#f47321] rounded-full text-white p-1" version="1.1" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 256 256" enable-background="new 0 0 256 256"
                xml:space="preserve">
                <g>
                  <g>
                    <g>
                      <path fill="#fff"
                        d="M124.1,10.8c-1,0.6-2.6,1.9-3.4,3l-1.5,2L119,67.4l-0.1,51.6H68c-56.6,0-53.2-0.2-56.4,3.9c-2.2,2.9-2.2,7.6,0,10.5c3.1,4.1-0.3,3.9,56.4,3.9h50.9V188c0,56.6-0.2,53.2,3.9,56.4c2.9,2.2,7.6,2.2,10.5,0c4.1-3.1,3.9,0.3,3.9-56.4v-50.9H188c56.6,0,53.2,0.2,56.4-3.9c2.2-2.9,2.2-7.6,0-10.5c-3.1-4.1,0.3-3.9-56.4-3.9h-50.9V68c0-56.5,0.2-53.2-3.8-56.3C130.8,9.9,126.8,9.4,124.1,10.8z" />
                    </g>
                  </g>
                </g>
              </svg>
              <p class="text-2xl font-Bahij text-[#f47321]">2</p>
              <svg class="w-7 h-7 bg-[#f47321] rounded-full text-white p-1" version="1.1" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 256 256" enable-background="new 0 0 256 256"
                xml:space="preserve">
                <g>
                  <g>
                    <g>
                      <path fill="#fff"
                        d="M15.3,119.7c-5.3,2.3-6.9,9.1-3.4,13.7c3,4-6.8,3.7,116.2,3.7c123.5,0,113.1,0.3,116.4-3.9c1.3-1.6,1.5-2.6,1.5-5.2c0-2.7-0.3-3.6-1.6-5.3c-3.1-4,6.2-3.8-116.4-3.8C37,119,16.7,119.1,15.3,119.7z" />
                    </g>
                  </g>
                </g>
              </svg>
                  
            </div>
            <div class="flex items-center justify-between p-3 basis-3/4 bg-[#f47321] text-white text-xl font-bold rounded-lg ml-10">
              <p>الإجمالي</p>
              <p>₪28</p>
            </div>
            <!-- <button type="button"
              class="w-full inline-flex justify-center rounded-md border border-transparent shadow-sm px-4 py-2 bg-orange-600 text-base font-medium text-white hover:bg-orange-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-orange-500 sm:ml-3 sm:w-auto sm:text-sm"
              @click="$emit('confirm')">
              إضافة
            </button>
            <button type="button"
              class="mt-3 w-full inline-flex justify-center rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-base font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm"
              @click="$emit('close')">
              إلغاء
            </button> -->
          </div>
        </div>
        <button type="button"
          class=" absolute top-2 left-2 mt-3 w-full inline-flex justify-center rounded-full border border-gray-300 shadow-sm px-4 py-2.5 bg-white text-3xl font-bold text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm "
          @click="$emit('close')">
          X
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.form-checkbox {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  background-color: #fff;
  border-color: black;
  border-width: 1px;
  border-radius: 50%;
  display: inline-block;
  vertical-align: middle;
  background-origin: border-box;
  user-select: none;
  flex-shrink: 0;
  color: currentColor;
  background-size: 100% 100%;
  background-position: center;
  background-repeat: no-repeat;
}

.form-checkbox:checked {
  background-image: url("data:image/svg+xml,%3csvg viewBox='0 0 16 16' fill='white' xmlns='http://www.w3.org/2000/svg'%3e%3cpath d='M5.707 7.293a1 1 0 0 0-1.414 1.414l2 2a1 1 0 0 0 1.414 0l4-4a1 1 0 0 0-1.414-1.414L7 8.586 5.707 7.293z'/%3e%3c/svg%3e");
  border-color: transparent;
  background-color: currentColor;
  background-size: 100% 100%;
  background-position: center;
  background-repeat: no-repeat;
}
</style>