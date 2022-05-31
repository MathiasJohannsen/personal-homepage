<template>
  <div class="slide-wrapper">
    <div id="slide-body" :class="slideDirection">
      <div class="h-screen w-screen">
        <div class="h-full w-full overflow-hidden">
          <div class="h-full w-full overflow-auto">
            <div class="h-screen w-full bg-orange-100">
              <h1 class="pt-10 text-4xl">Catan</h1>
              <h2 class="text-xl">Technology</h2>
              <ul class="list-none">
                <li>Unity</li>
              </ul>
            </div>
            <div class="h-screen w-full bg-lime-100">
              <h1 class="pt-10 text-4xl">Minesweeper 3D</h1>
            </div>
            <div class="h-screen w-full bg-yellow-100">
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
