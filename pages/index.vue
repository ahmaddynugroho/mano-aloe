<template>
  <div class="flex flex-wrap justify-center">
    <div>
      <div v-for="(msg, i) in messages" :key="i">
        <Card1
          v-if="i < messages.length / 2"
          :author="msg.Name"
          :native="msg.Native_message"
          :en="msg.EN_message"
          :jp="msg.JP_message_Deepl"
        />
      </div>
    </div>
    <div>
      <div v-for="(msg, i) in messages" :key="i">
        <Card1
          v-if="i >= messages.length / 2"
          :author="msg.Name"
          :native="msg.Native_message"
          :en="msg.EN_message"
          :jp="msg.JP_message_Deepl"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Card1 from '@/components/cards/Card1'
import json from '@/static/Aloe_Appreciation_Messages.json'

export default {
  components: {
    Card1,
  },
  data() {
    return {
      messages: json,
    }
  },
}
</script>

<style></style>
