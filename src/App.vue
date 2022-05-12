<template>
  <!-- <NavbarComponent/> -->
  <router-view/>
</template>

<script>
import NavbarComponent from '@/components/NavbarComponent.vue'

export default {
  components: {
    NavbarComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.navigation-element {
  display: flex;
  justify-content: space-around;
  transition-duration: 0.7s;
}

.navigation-element span {
  padding-inline: 5px;
}

.tracking-full-width {
  flex-direction: row;
}

:hover.tracking-full-width {
  width: 100vw;
  color: red;
}

.tracking-full-height {
  height: 0px;
}

:hover.tracking-full-height {
  height: 100vh;
  color: red;
}

.turn-right span {
  transform: rotate(90deg);
}

.turn-left span {
  transform: rotate(-90deg);
}
</style>
