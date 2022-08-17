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
                <p class="px-8 leading-10">
                  <span class="p-2 m-2 rounded-lg whitespace-nowrap bg-[#FED7B3]">🕒 2021</span>
                
                  <span class="p-2 m-2 rounded-lg whitespace-nowrap bg-[#FED7B3]">🎮 Unity</span>
                
                  <a href="https://github.com/MathiasJohannsen/unity-catan" target="_blank">
                    <span class="p-2 m-2 rounded-lg whitespace-nowrap bg-[#FED7B3]">🔗 Github</span>
                  </a>
                </p>
                <br>
                <br>
                <p class="px-8">
                  This project is still ongoing. The game will have the same basic rules as the boardgame but the world is endless and waits to be discovered by the player.
                </p>
              </div>
              <div class="h-screen w-1/2 bg-image bg-catan">
              </div>
            </div>

            <div class="h-screen w-full bg-lime-100" style="background-color: #FEFFDE; color: #52734D;">
              <h1 class="pt-10 text-4xl">That's not all</h1>
              <br>
              <p>I will add more of my Projects to my Website soon...</p>
            </div>
            <!-- <div class="h-screen w-full bg-lime-100" style="background-color: #FEFFDE; color: #52734D;">
              <h1 class="pt-10 text-4xl">Minesweeper 3D</h1>
            </div>
            <div class="h-screen w-full bg-yellow-100" style="background-color: #EBFFFA; color: #0DCEDA;">
              <h1 class="pt-10 text-4xl">Real World Simulator</h1>
            </div> -->
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
.bg-catan {
  background-image: url('@/assets/img/catan.png');
}
</style>
