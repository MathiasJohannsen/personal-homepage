<template>
  <div class="slide-wrapper">
    <div id="slide-body" :class="slideDirection">
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
  height: 100vh;
}

#slide-body {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
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

.slide-wrapper #slide-body.slide-bottom {
  transition: 1s;
  top: -100vw;
}
</style>
