<template>
  <div class="flex flex-wrap justify-center">
    <div>
      <div v-for="(msg, i) in messages" :key="i">
        <Card1
          v-if="i < messages.length / 2"
          :author="msg.author"
          :en="msg.en"
          :jp="msg.jp"
        />
      </div>
    </div>
    <div>
      <div v-for="(msg, i) in messages" :key="i">
        <Card1
          v-if="i >= messages.length / 2"
          :author="msg.author"
          :en="msg.en"
          :jp="msg.jp"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Card1 from '@/components/cards/Card1'

export default {
  components: {
    Card1,
  },
  data() {
    return {
      messages: [
        {
          author: 'Y E S man ',
          en:
            'Tempor consequat dolor ex est amet tempor do incididunt dolor aliqua fugiat. Pariatur cupidatat tempor anim veniam duis labore mollit. Ex cupidatat anim nisi ipsum magna amet anim laboris amet ipsum ad irure id.',
          jp: 'ペコです',
        },
      ],
    }
  },
}
</script>

<style></style>
