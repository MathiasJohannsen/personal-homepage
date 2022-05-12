<template>
  <div class="h-screen w-100vw bg-orange-100">
    <h1 class="pt-10 text-4xl">
      Catan
    </h1>
    <h2 class="text-xl">
      Technology
    </h2>
    <ul class="list-disc">
      <li>Unity</li>
    </ul>
  </div>
  <div class="h-screen w-100vw bg-lime-100">
    <h1 class="pt-10 text-4xl">
      Minesweeper 3D
    </h1>
  </div>
  <div class="h-screen w-100vw bg-yellow-100">
    <h1 class="pt-10 text-4xl">
      Real World Simulator
    </h1>
  </div>

  <div class="fixed left-0 top-0 bottom-0">
    <div class="flex items-center h-screen">
      <router-link
        to="/"
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
      </router-link>
    </div>
  </div>
</template>
