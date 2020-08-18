<template>
  <div
    class="mx-3 my-6 rounded-lg px-4 py-4 text-pink-200 bg-local bg-cover transform hover:-translate-y-2 transition ease-out duration-200 hover:shadow-2xl float max-w-md"
    :style="{ 'background-image': `url(${require('@/assets/img/bg.jpg')})` }"
  >
    <div v-if="en.length < 130">
      <span v-if="enLang" class="text-2xl">"{{ en }}"</span>
      <span v-else class="text-2xl">"{{ jp }}"</span>
    </div>
    <div v-if="en.length >= 130">
      <span v-if="enLang">"{{ en }}"</span>
      <span v-else>"{{ jp }}"</span>
    </div>
    <div class="h-12"></div>
    <span class="absolute bottom-0 right-0 mr-3 mb-1 font-light text-sm"
      >- {{ author }}</span
    >
  </div>
</template>

<script>
export default {
  props: ['author', 'en', 'jp'],
  data() {
    return {
      enLang: true,
    }
  },
}
</script>

<style>
.float:hover {
  -webkit-box-shadow: 0px 0px 17px 0px rgba(255, 240, 255, 1);
  -moz-box-shadow: 0px 0px 17px 0px rgba(255, 240, 255, 1);
  box-shadow: 0px 0px 17px 0px rgba(255, 240, 255, 1);
}
</style>
