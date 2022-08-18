<template>
  <div class="slide-wrapper">
    <div id="slide-body" :class="slideDirection">
      <div class="flex h-screen items-center justify-center bg-green-200">
        <p class="font-bold text-[4vw]">m.johannsen.privat@gmail.com</p>
      </div>
      <!-- <NavbarComponent title="HOME" align="top-0 left-0 right-0" color="text-gray-400" padding="pt-3 pb-3 md:pt-10" tracking=""/> -->
      <div class="absolute top-0 left-0 right-0">
        <div class="flex justify-center">
          <p
            @click="slide('/', 'slide-top')"
            class="
              text-gray-900
              pt-3
              md:pt-10
              pb-3
              w-0
              navigation-element
              tracking-full-width
              font-bold
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
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HomeView",
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
</style>
