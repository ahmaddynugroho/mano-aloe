<template>
  <div class="antialiased relative text-center">
    <Landing />
    <Nuxt class="" />
    <NavMenu />
  </div>
</template>

<script>
import NavMenu from '@/components/NavMenu'
import Landing from '@/components/Landing'
export default {
  name: 'Layout',
  components: {
    NavMenu,
    Landing,
  },
}
</script>
<style>
body {
  background-color: #0e020c;
}
</style>
