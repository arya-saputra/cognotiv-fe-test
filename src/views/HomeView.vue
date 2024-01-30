<template>
  <div class="Home w-full h-[100vh] overflow-hidden text-[#fba900] bg-[url(/pattern.jpeg)] bg-cover	">
    <div class="page-1 container relative mx-auto max-w-[1280px] mt-10"
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
        class="transition-all image w-[80%] mx-auto mt-[-160px] h-[63vh] overflow-hidden relative z-[10]"
        :class="{ 'opacity-0':page==2, 'opacity-100 duration-1000 delay-1000':page==1 }">
        <img
          src="@/assets/image.jpeg"
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
    <div class="page-2 container relative text-black"
      :class="{ 'opacity-100':page==2, 'opacity-0':page==1 }">
      <div class="fixed top-[20px] left-[20px] text-[20px] z-[100] text-[#fff] cursor-pointer"
      :class="{ 'opacity-100':page==2, 'opacity-0':page==1 }"
      @click="page=1"><span class="mr-3">←</span>back</div>
      
      <!-- ACCENTS -->
      <div
        class="transition-all fixed top-0 bg-[#fba900] h-[20vh] z-[50]"
        :class="{ 'w-full  delay-300':menu==1, 'w-[0%]':menu!==1 }">
      </div>
      <div
        class="transition-all fixed top-0 bg-[#fba900] h-[20vh] z-[50]"
        :class="{ 'w-full  delay-300':menu==2, 'w-[0%]':menu!==2 }">
      </div>
      <div
        class="transition-all fixed top-0 bg-[#fba900] h-[20vh] z-[50]"
        :class="{ 'w-full  delay-300':menu==3, 'w-[0%]':menu!==3 }">
      </div>

      <!-- MENU -->
      <div class="menu fixed bottom-0 left w-[60%] text-[6vw] py-20 pl-[8%] z-[200]"
        :class="{ 'opacity-0':page==1 }">
        <div class="menu-opt font-bold flex items-center cursor-pointer"
          :class="{ 'text-[#fba900]':menu==1 }"
          @click="menu=1">
          <div class="duration-1000 h-[10px] mr-[20px] w-[10%]">
            <div class="transition-all h-full bg-[#fba900]" :class="{ 'delay-300 w-full':menu==1, 'delay-300 w-[0%]':menu!=1 }"></div>
          </div>
          About Us
        </div>
        <div class="menu-opt font-bold flex items-center cursor-pointer"
          :class="{ 'text-[#fba900]':menu==2 }"
          @click="menu=2">
          <div class="duration-1000 h-[10px] mr-[20px] w-[10%]">
            <div class="transition-all h-full bg-[#fba900]" :class="{ 'delay-300 w-full':menu==2, 'delay-300 w-[0%]':menu!=2 }"></div>
          </div>
          Our Product
        </div>
        <div class="menu-opt font-bold flex items-center cursor-pointer"
          :class="{ 'text-[#fba900]':menu==3 }"
          @click="menu=3">
          <div class="duration-1000 h-[10px] mr-[20px] w-[10%]">
            <div class="transition-all h-full bg-[#fba900]" :class="{ 'delay-300 w-full':menu==3, 'delay-300 w-[0%]':menu!=3 }"></div>
          </div>
          Contact Us
        </div>
      </div>

      <!-- MENU 1 -->
      <div class="transition-all delay-300 duration-500 fixed z-[200] top-0 right-0 opacity-100 w-[67%] h-[100vh] flex items-center justify-center"
        :class="{ 'right-[-80%] opacity-0':menu!==1 }">
        <div class="relative mx-auto w-[50%]">
          <div class="transition-all delay-1000 webel-1 h-[10px] absolute left-[-30px] top-[-30px] bg-[#fba900]"
            :class="{ 'w-[15%] opacity-100':menu==1, 'w-0 opacity-0':menu!=1 }">
          </div>
          <div class="transition-all delay-1000 webel-2 h-[20%] w-[10px] absolute left-[-30px] top-[-30px] bg-[#fba900]"
            :class="{ 'h-[15%] opacity-100':menu==1, 'h-0 opacity-0':menu!=1 }">
          </div>
          <div class="bg-[rgba(255,255,255,.5)] p-5 rounded-lg">
            <div class="text-[5vw] font-bold">
              Our People Come First
            </div>
            <div class="text-[30px] font-bold">
              We are independently
              owned, strategic
              creative agency forever
              curious and ready to
              transform the way
              business is done.
            </div>
          </div>
          <div class="w-full text-right mt-5">
            <button class="rounded-lg font-bold bg-[#fba900] text-[#fff] text-[30px] py-[10px] px-[30px]">Learn more</button>
          </div>
        </div>
        
      </div>

      <!-- MENU 2 -->
      <div class="transition-all delay-300 duration-500 fixed z-[200] top-0 right-0 w-[67%] h-[100vh] flex items-center justify-center"
        :class="{ 'left-[45%] opacity-100':menu==2, 'left-[-80%] opacity-0':menu!==2  }">
        <div class="relative mx-auto w-[70%] overflow-hidden flex">
          <div class="transition-all p-20 bg-[rgba(255,255,255,.5)] rounded-lg text-[80px] font-bold mr-[40px]"
            :class="{ 'ml-[-80%]':content==2, 'ml-0':content==1 }">
            <div class="font-bold">We Know You have</div>
            <div class="font-bold animate-blink">PROBLEM</div>
          </div>
          <div class="p-20 bg-[rgba(255,255,255,.5)] rounded-lg text-[80px] font-bold">
            <div class="font-bold">We Solve Your</div>
            <div class="font-bold animate-blink">PROBLEM</div>
          </div>

          <div class="absolute h-full flex items-center right-[60px] cursor-pointer" @click="content==1?content=2:content=1">
            <div class="w-[100px] h-[100px] bg-[#fba900] rounded-[50%] flex items-center justify-center text-[4vw]">
              ▶
            </div>
          </div>
        </div>
      </div>

      <!-- MENU 3 -->
      <div class="transition-all delay-300 duration-500 fixed z-[200] top-0 right-0 opacity-100 w-[67%] h-[100vh] flex items-center justify-center"
        :class="{ 'right-[-80%] opacity-0':menu!==3 }">
        <div class="relative mx-auto w-[50%]">
          <div class="transition-all delay-1000 webel-1 h-[10px] absolute left-[-30px] top-[-30px] bg-[#fba900]"
            :class="{ 'w-[15%] opacity-100':menu==3, 'w-0 opacity-0':menu!=3 }">
          </div>
          <div class="transition-all delay-1000 webel-2 h-[20%] w-[10px] absolute left-[-30px] top-[-30px] bg-[#fba900]"
            :class="{ 'h-[15%] opacity-100':menu==3, 'h-0 opacity-0':menu!=3 }">
          </div>
          <div class="bg-[rgba(255,255,255,.5)] p-10 rounded-lg">
            <div class="text-[3vw] font-[600]">
              <div class="font-[600]">Type your beautiful name
              </div>
              <input placeholder="in here of course :)" class="w-full p-4 mt-3 rounded-lg" />
            </div>
            <div class="text-[3vw] font-[600]">
              <div class="font-[600]">Type your beautiful name
              </div>
              <input placeholder="in here of course :)" class="w-full p-4 mt-3 rounded-lg" />
            </div>
            <button class="w-full mt-7 rounded-lg font-bold bg-[#fba900] text-[#fff] text-[30px] py-[10px] px-[30px]">Submit</button>
          </div>
          <div class="transition-all delay-1000 webel-1 h-[10px] absolute right-[-30px] bottom-[-30px] bg-[#fba900]"
            :class="{ 'w-[15%] opacity-100':menu==3, 'w-0 opacity-0':menu!=3 }">
          </div>
          <div class="transition-all delay-1000 webel-2 h-[20%] w-[10px] absolute right-[-30px] bottom-[-30px] bg-[#fba900]"
            :class="{ 'h-[15%] opacity-100':menu==3, 'h-0 opacity-0':menu!=3 }">
          </div>
        </div>
        
      </div>
    </div>

    <!-- BG IMAGE -->
    <div class="transition-all duration-200 fixed z-[100]"
      :class="{ 'top-0 right-0 opacity-100 w-[67%] h-[100vh]':page==2, ' h-[20px] w-[20px] top-[60%] right-[60%] opacity-0':page==1 }">
      <div class="relative transition-all ease-out h-[100vh]"
        :class="{ 'top-0':menu==1, 'top-[-100vh]':menu==2, 'top-[-200vh]':menu==3 }">
        <img src="@/assets/image-2.jpeg" class="transition-all duration-200 w-full h-full" :class="{ 'delay-500 grayscale':menu==1 }" />
        <img src="@/assets/image-3.jpeg" class="transition-all duration-200 w-full h-full" :class="{ 'delay-500 grayscale':menu==2 }" />
        <img src="@/assets/image-4.jpeg" class="transition-all duration-200 w-full h-full" :class="{ 'delay-500 grayscale':menu==3 }" />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { ref } from "vue";

const hover = ref(false);
const btnHover = ref(false);
const page = ref(1);
const menu = ref(1);
const content = ref(1);
</script>
<style>
.animate-blink {
  animation: blink 1s infinite;
}

@keyframes blink {
  0% {
    color:white;
  }
  50% {
    color: #fba900;
  }
  100% {
    color:white;
  }
}
</style>