<template>
  <div class="antialiased relative text-center">
    <div>
      <img class="w-full" src="../assets/img/header.jpg" />
      <Nuxt class="" />
    </div>
    <div class="fixed bottom-0 right-0">
      <button
        class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
      >
        Home</button
      ><br />
      <button
        class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
      >
        About
      </button>
    </div>
  </div>
</template>

<style>
body {
  background-color: #0e020c;
}
</style>
