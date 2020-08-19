<template>
  <div
    v-show="toggleMenu"
    class="fixed bottom-0 right-0"
    @mouseleave="showlangmenu = false"
  >
    <nuxt-link to="/">
      <button
        class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
      >
        Home
      </button>
    </nuxt-link>
    <br />
    <nuxt-link to="/about">
      <button
        class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
      >
        About
      </button>
    </nuxt-link>
    <br />
    <nuxt-link to="/latest">
      <button
        class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
      >
        Latest👅Posts
      </button>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  data: () => ({
    open: true,
  }),
  methods: {
    toggleMenu() {
      console.log(this.open)
      this.open = !this.open
    },
  },
}
</script>
<style>
/*  */
.menu-enter-active,
.menu-leave-active {
  transition: transform 0.2s ease;
}

.slide-enter-active,
.slide-leave-active {
  transition: transform 0.2s ease;
}

.menu-enter,
.menu-leave-to {
  transform: translateX(-100%);
  transition: all 150ms ease-in 0s;
}

.sidebar-backdrop {
  background-color: rgba(0, 0, 0, 0.5);
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  cursor: pointer;
}

.sidebar-panel {
  overflow-y: auto;
  background-color: #130f40;
  position: fixed;
  left: 0;
  top: 0;
  height: 100vh;
  z-index: 999;
  padding: 3rem 20px 2rem 20px;
  width: 300px;
}
</style>
