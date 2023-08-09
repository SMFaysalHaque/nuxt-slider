<!-- Please remove this file from your project -->
<template>
  <div>
    <div class="flex justify-center items-center min-h-screen w-full md:w-[1500px] mx-auto">
      <div>
        <button @click="previousSlide()" id="prev" class="border px-4 mr-2">prev</button>
      </div>
      <div id="scrlBody" class="flex w-[400px] md:w-[1200px] h-[100px] border-4 border-black overflow-x-hidden flex-row">
        <div class="flex flex-row">
          <div class="item min-w-[400px] h-auto border border-red-500">
          1
          </div>
          <div class="item min-w-[400px] h-auto border border-green-500">
            2
          </div>
          <div class="item min-w-[400px] h-auto border border-blue-500">
            3
          </div>
          <div class="item min-w-[400px] h-auto border border-pink-500">
            4
          </div>
          <div class="item min-w-[400px] h-auto border border-purple-500">
            5
          </div>
          <div class="item min-w-[400px] h-auto border border-pink-500">
            6
          </div>
        </div>
      </div>
      <div>
        <button @click="nextSlide()" id="Slide" class="border-4 px-4 ml-2">next</button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      nextSlide(){
        // const element = document.getElementById("scrlBody");
        // let x = element.scrollLeft += 400;
        // console.log("Q", element.scrollLeft);
        // console.log("A", x);

        let sliderMain = document.getElementById('scrlBody');
        let item = sliderMain.getElementsByClassName('item');
        sliderMain.append(item[0]);
        
      },
      previousSlide(){
        // const element = document.getElementById("scrlBody");
        // element.scrollLeft -= 400;
        let sliderMain = document.getElementById('scrlBody');
        let item = sliderMain.getElementsByClassName('item');
        sliderMain.prepend(item[item.length - 1]);
      },
    }
  }
</script>

<style scoped>
#scrlBody{
  scroll-behavior: smooth;
}
</style>
