<template>
  <div class="slide-wrapper">
    <div id="slide-body" :class="slideDirection">
      <div class="h-screen w-screen">
        <div class="h-full w-full overflow-hidden">
          <div class="h-full w-full overflow-auto">
            <div class="flex">
              <div class="h-screen w-1/2 bg-[#FCECDD] text-[#FF6701]">
                <h1 class="pt-10 text-4xl">Catan</h1>
                <br>
                <p>
                  <span class="p-2 rounded-lg bg-[#FED7B3]">🕒 2021</span>
                </p>
                <br>
                <p>
                  <span class="p-2 rounded-lg bg-[#FED7B3]">🎮 Unity</span>
                </p>
                <br>
                <p>
                  <a href="https://github.com/MathiasJohannsen/unity-catan" target="_blank">
                    <span class="p-2 rounded-lg bg-[#FED7B3]">🔗 Github</span>
                  </a>
                </p>
                <br>
              </div>
              <div class="h-screen w-1/2 bg-image bg-[url('@/assets/img/catan.png')]">

              </div>
            </div>
            <div class="h-screen w-full bg-lime-100" style="background-color: #FEFFDE; color: #52734D;">
              <h1 class="pt-10 text-4xl">Minesweeper 3D</h1>
            </div>
            <div class="h-screen w-full bg-yellow-100" style="background-color: #EBFFFA; color: #0DCEDA;">
              <h1 class="pt-10 text-4xl">Real World Simulator</h1>
            </div>
          </div>
          <div class="absolute left-0 top-0 bottom-0">
            <div class="flex items-center h-screen">
              <p
                @click="slide('/', 'slide-left')"
                class="
                  text-gray-900
                  pr-3
                  pl-3
                  md:pl-10
                  navigation-element
                  tracking-full-height
                  turn-right
                  font-bold
                  flex-col
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
.slide-wrapper {
  position: relative;
  overflow: hidden;
  width: 100vw;
  height: fit-content;
  /* background-color: #efdddd; */
}

#slide-body {
  position: fixed;
  right: 0;
  left: 0;
  width: 100vw;
  height: fit-content;
  transition: 1s;
}

.slide-wrapper #slide-body.slide-left {
  transition: 1s;
  left: 100vw;
}

.slide-wrapper #slide-body.slide-right {
  transition: 1s;
  left: -100vw;
}
</style>
