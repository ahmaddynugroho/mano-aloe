<template>
  <div>
    <div
      class="fixed bottom-0 right-0"
      v-on:click="openMenu"
      @mouseover="openMenu"
      @mouseleave="closeMenu"
    >
      <button
        class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
      >
        <img src="/1200px-Hamburger_icon.svg.jpg" class="img-icon" />
      </button>
      <div class="fixed second-bottom right-0" v-if="open">
        <nuxt-link to="/">
          <button
            class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
          >
            <img src="/home_icon.png" class="img-icon" />
          </button>
        </nuxt-link>
        <br />
        <nuxt-link to="/about">
          <button
            class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
          >
            <img src="/about_icon.jpg" class="img-icon" />
          </button>
        </nuxt-link>
        <br />
        <nuxt-link to="/latest">
          <button
            class="transition duration-150 ease-out hover:scale-105 transform hover:-translate-y-1 bg-pink-200 shadow hover:shadow-xl active:bg-red-500 text-pink-900 rounded-full px-4 py-1 mx-4 mb-2"
          >
            <img
              src="/416-4164629_latest-announcement-latest-news-icon-latest-news-icon-png.png"
              class="img-icon"
            />
          </button>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<!-- Could not use one toggleMenu function because both mouseclick & mousehover toggle, so first click would mess up order -->
<script>
export default {
  data: () => ({
    open: true,
  }),
  methods: {
    openMenu() {
      this.open = true
      console.log(this.open)
    },
    closeMenu() {
      this.open = false
      console.log(this.open)
    },
  },
}
</script>
<style>
.img-icon {
  max-height: 3vw;
  max-width: 3vw;
}

.second-bottom {
  bottom: 4vw;
}
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
