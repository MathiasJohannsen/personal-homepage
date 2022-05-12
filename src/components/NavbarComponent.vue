<template>
  <div :class="'fixed ' + this.align">
    <div class="flex justify-center">
      <router-link
        to="/about"
        :class="
          this.color +
          ' ' +
          this.padding +
          ' ' +
          this.tracking +
          ' navigation-element font-bold'
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
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default {
  props: {
    title: String,
    align: String,
    color: String,
    padding: String,
    tracking: String,
  },
};
</script>

<style scoped>
nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

  <!-- <NavbarComponent title="HOME" align="top-0 left-0 right-0" color="text-gray-400" padding="pt-3 pb-3 md:pt-10" tracking=""/> -->
  <!-- <NavbarComponent title="CONTACT" align="bottom-0 left-0 right-0" color="text-gray-900" padding="pt-3 pb-3 md:pb-10" tracking="tracking-full-width w-0"/> -->
