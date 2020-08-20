<template>
  <div class="antialiased relative text-center">
    <ContactNavbar />
    <Landing />
    <Nuxt class="" />
    <NavMenu />
  </div>
</template>

<script>
import ContactNavbar from '@/components/ContactNavbar'
import NavMenu from '@/components/NavMenu'
import Landing from '@/components/Landing'
export default {
  name: 'Layout',
  components: {
    ContactNavbar,
    NavMenu,
    Landing,
  },
}
</script>
<style>
body {
  background-color: #0e020c;
  color: #ffffff;
}
</style>
