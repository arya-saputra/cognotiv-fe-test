<template>
  <div class="Home w-full h-[100vh] text-[#fba900]">
    <div class="page-1 container relative"
      @mouseover="hover=true"
      @mouseleave="hover=false">
      <div class="bar-group transition-all delay-300 duration-1000 right-0 top-0 absolute h-[10px] w-[30%] flex justify-end gap-2"
        :class="{ 'top-[-100%] opacity-0':page==2 }">
        <div class="bar-1 transition-all delay-300 duration-1000 h-[10px] bg-[#fba900]"
          :class="{ 'w-[10%]':hover, 'w-0':!hover }"></div>
        <div class="bar-2 transition-all delay-300 duration-1000 h-[10px] bg-[#fba900]"
          :class="{ 'w-[30%]':hover, 'w-0':!hover }"></div>
      </div>
      <h1
        class="transition-all delay-300 duration-1000 ease-in-out text-[200px] font-bold relative z-[100] top-[0]"
        :class="{ 'text-[206px]':hover,'mt-[-80%]':page==2 }">We Create</h1>
      <div
        class="image w-[80%] mx-auto mt-[-160px] h-[63vh] overflow-hidden relative z-[10]"
        :class="{ 'opacity-0':page==2 }">
        <img
          src="/image.jpeg"
          class="transition-all delay-300 duration-1000 ease-in-out  w-full grayscale"
          :class="{ 'scale-[1.1] grayscale-[0]':hover }" />
      </div>
      <div
        @mouseover="btnHover=true"
        @mouseleave="btnHover=false"
        @click="page=2">
        <div
          class="transition-all delay-300 duration-1000 ease-out font-bold left-[-90%] text-[90px] mt-[-80px] z-[100] absolute opacity-0" 
          :class="{ 'left-[0%] cursor-pointer opacity-100':hover, 'text-[white]':btnHover, 'bottom-[-400%] opacity-0':page==2 }">AWESOME THINGS</div>
        <div
          class="transition-all delay-300 duration-1000	 ease-out font-bold right-[-40%] text-[100px] mt-[-150px] z-[100] absolute bottom-[-60px] opacity-0"
          :class="{ 'right-[20%] cursor-pointer opacity-100':hover, 'text-[white]':btnHover, 'bottom-[-400%] opacity-0':page==2 }">→</div>
        <div
          class="transition-all delay-300 duration-1000 ease-out font-bold left-[-100%] text-[90px] mt-[-60px] z-[0] absolute bg-[#fba900] w-[85%] h-[100px] rounded opacity-0 z-[10]"
          :class="{ 'left-[-2%] opacity-100':btnHover, 'bottom-[-400%] opacity-0':page==2 }"></div>
      </div>
    </div>
    <div class="page-2 container relative">
      <div class="transition-all duration-200 fixed"
        :class="{ 'top-0 right-0 opacity-100 w-[67%] h-[100vh]':page==2, ' h-[20px] w-[20px] top-[100px] right-[60%] opacity-0':page==1 }">
        <img src="/image.jpeg" class="w-full h-full" />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { ref } from "vue";

const hover = ref(false);
const btnHover = ref(false);
const page = ref(1);
</script>