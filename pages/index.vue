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
        {
          author: 'Y E S man',
          en:
            'Mollit minim dolore culpa duis anim tempor consequat laborum culpa occaecat duis fugiat reprehenderit.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en: 'Ut id ullamco sit fugiat laboris magna adipisicing nostrud.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en:
            'Culpa occaecat sit commodo eu ex cupidatat dolor aliqua. Eu sint duis laboris nulla ullamco dolor culpa nostrud. Reprehenderit cupidatat dolor dolor occaecat Lorem voluptate dolor proident ipsum Lorem sit non officia. Ut ullamco Lorem nostrud fugiat mollit velit aliqua sit et occaecat. Mollit amet voluptate cupidatat laboris voluptate magna in cupidatat. Veniam enim culpa proident velit culpa nulla eiusmod magna. Esse quis velit consequat sit reprehenderit voluptate.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en:
            'Enim proident et tempor commodo nisi excepteur in consequat. Fugiat nostrud et ad dolore consequat laboris aliquip velit ea. Amet est ut deserunt sit in fugiat. Ut tempor irure ad consectetur. Quis aliqua do laboris magna minim ipsum excepteur sint excepteur nisi. Dolore sint tempor pariatur laboris incididunt mollit labore fugiat nostrud cillum magna et. Cillum dolore eu qui incididunt et cillum.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en: 'Culpa nulla aute eu enim nostrud.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en: 'Enim in eu cupidatat proident.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en: 'Lorem et do ipsum ea ut qui cupidatat eiusmod eiusmod esse.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en:
            'Sunt consequat ut cupidatat adipisicing commodo enim et est exercitation commodo laborum est voluptate amet. Laboris pariatur culpa enim ipsum tempor duis enim tempor eu pariatur id nostrud nostrud. Cillum ea pariatur commodo sint labore do laborum irure nostrud cillum. Enim non excepteur deserunt cillum adipisicing mollit voluptate excepteur incididunt.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en:
            'Magna pariatur duis nostrud officia ad velit officia culpa. Lorem labore in mollit eiusmod mollit aute mollit minim anim laborum. Veniam culpa officia sunt cupidatat enim occaecat occaecat do aliqua qui est ut cillum elit. Excepteur sit aute irure exercitation in duis fugiat nostrud do dolor amet ea irure aliquip. Incididunt proident sint ea ullamco duis eiusmod.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en:
            'Enim enim ipsum sunt quis et veniam occaecat aute consequat quis ad nisi deserunt deserunt.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en:
            'Culpa et id reprehenderit laborum amet ex voluptate duis incididunt.',
          jp: 'ペコです',
        },
        {
          author: 'Y E S man',
          en:
            'Excepteur non sint occaecat ex in ex elit anim laboris consectetur proident amet anim.',
          jp: 'ペコです',
        },
      ],
    }
  },
}
</script>

<style></style>
