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
  <!-- <NavbarComponent title="HOME" align="top-0 left-0 right-0" color="text-gray-400" padding="pt-3 pb-3 md:pt-10" tracking=""/> -->
  <div class="fixed top-0 left-0 right-0">
    <div class="flex justify-center">
      <p
        class="
          text-gray-400
          pt-3
          md:pt-10
          pb-3
          w-0
          navigation-element
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
  <!-- <NavbarComponent title="CONTACT" align="bottom-0 left-0 right-0" color="text-gray-900" padding="pt-3 pb-3 md:pb-10" tracking="tracking-full-width w-0"/> -->
  <div class="fixed bottom-0 left-0 right-0">
    <div class="flex justify-center">
      <router-link
        to="/about"
        class="
          text-gray-900
          pt-3
          pb-3
          md:pb-10
          w-0
          navigation-element
          tracking-full-width
          font-bold
        "
      >
        <span>C</span>
        <span>O</span>
        <span>N</span>
        <span>T</span>
        <span>A</span>
        <span>C</span>
        <span>T</span>
      </router-link>
    </div>
  </div>
  <div class="fixed right-0 top-0 bottom-0">
    <div class="flex items-center h-screen">
      <router-link
        to="/projects"
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
        <span>P</span>
        <span>R</span>
        <span>O</span>
        <span>J</span>
        <span>E</span>
        <span>C</span>
        <span>T</span>
        <span>S</span>
      </router-link>
    </div>
  </div>
  <div class="fixed left-0 top-0 bottom-0">
    <div class="flex items-center h-screen">
      <router-link
        to="/about"
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
        <span>A</span>
        <span>B</span>
        <span>O</span>
        <span>U</span>
        <span>T</span>
      </router-link>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "@/components/HelloWorldComponent.vue"; // @ is an alias to /src
import NavbarComponent from "@/components/NavbarComponent.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    HelloWorld,
    NavbarComponent
  },
});
</script>
