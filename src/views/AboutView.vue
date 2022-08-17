<template>
  <div class="slide-wrapper">
    <div id="slide-body" :class="slideDirection">
      <div class="h-screen w-screen">
        <div class="h-full w-full overflow-hidden">
          <div class="h-full w-full overflow-auto">
            <div class="flex">
              <div class="h-screen w-1/2 bg-[#CDFFEB] text-[#07456F]">
                <h1 class="pt-10 text-4xl">This is me ...</h1>
                <br><br><br>
                <h1 class="pt-10 text-4xl">... and this is what i do and like ...</h1>
              </div>
              <div class="h-screen w-1/2 bg-image bg-portrait">
              </div>
            </div>
            <div class="h-screen w-full bg-image bg-git text-[beige]">
              <h1 class="pt-10 text-4xl"><div class="backdrop-blur-md">I learned programming in school and like to make many small projects in my free time </div></h1>
            </div>
            <div class="h-screen w-full bg-image bg-sax" style="background-color: #FCECDD; color: #FF6701;">
              <h1 class="pt-10 text-4xl">I play the saxophone</h1>
            </div>
            <div class="flex">
              <div class="h-screen w-1/2 bg-image bg-hills text-[#FFCDDD]">
                <h1 class="pt-10 text-4xl">I like to climb hills</h1>
              </div>
              <div class="h-screen w-1/2 bg-image bg-bike text-[lightgreen]">
                <h1 class="pt-10 text-4xl">and travel the world on my bike.</h1>
              </div>
            </div>
          </div>
          <div class="absolute right-0 top-0 bottom-0">
            <div class="flex items-center h-screen">
              <p
                @click="slide('/', 'slide-right')"
                class="
                  text-gray-900
                  pr-3
                  md:pr-10
                  pl-3
                  navigation-element
                  tracking-full-height
                  turn-left
                  font-bold
                  flex-col-reverse
                "
              >
                <span>H</span>
                <span>O</span>
                <span>M</span>
                <span>E</span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "AboutView",
  data() {
    return {
      slideDirection: "",
    };
  },
  methods: {
    slide(destination: string, direction: string) {
      this.slideDirection = direction;
      setTimeout(() => {
        this.$router.push(destination);
      }, 1000);
    },
  },
});
</script>

<style>
.bg-portrait {
  background-image: url('@/assets/img/portrait.jpg');
  background-position: center 80%;
}

.bg-git {
  background-image: url('@/assets/img/git.jpg');
}

.bg-sax {
  background-image: url('@/assets/img/sax.jpg');
}

.bg-hills {
  background-image: url('@/assets/img/hills.jpg');
}

.bg-bike {
  background-image: url('@/assets/img/bike.jpg');
}
</style>
