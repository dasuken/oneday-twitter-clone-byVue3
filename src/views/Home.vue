<template>
  <div class="home">
    <div class="text-white">
      <Tweet v-for="tweet in tweets" :key="tweet._id" :tweet="tweet" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue'
import vtweets from '@/tweets.js'
import Tweet from '@/components/Tweet.vue'

export default {
  name: 'Home',
  components: {
    Tweet
  },
  setup() {
    const tweets = ref(vtweets);
    return {
      tweets,
    }
  }
}
</script>
