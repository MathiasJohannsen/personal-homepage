<template>
  <div class="flex h-screen items-center justify-center">
    <div class="grid grid-cols-1 md:grid-cols-2 items-center gap-20">
      <div class="w-2/3 md:place-self-end md:self-center justify-self-center">
        <img
          class="w-full h-full"
          src="@/assets/img/MathiasJohannsen.svg"
          alt="Mathias Johannsen"
        />
      </div>
      <div class="w-1/3 justify-self-center md:justify-self-start">
        <img class="w-full h-full" src="@/assets/img/round-logo.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "@/components/HelloWorldComponent.vue"; // @ is an alias to /src

export default defineComponent({
  name: "HomeView",
  components: {
    // eslint-disable-next-line vue/no-unused-components
    HelloWorld,
  },
});
</script>
