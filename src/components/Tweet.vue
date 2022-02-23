<template>
  <div
    v-for="tweet in tweets"
    :key="tweet.id"
    class="tweet group group-hover:text-slate-300"
  >
    <div class="text-1xl lg:text-xl mb-16 flex-grow whitespace-normal">
      {{ tweet.content }}
    </div>
    <div class="grid grid-cols-2">
      <div
        class="text-blue-500 group-hover:text-slate-300 transition-all ease-in duration-75"
      >
        <a
          target="_blank"
          rel="noopener"
          href="https://twitter.com/intent/tweet?text=`${tweet.content}`"
          >Tweet me</a
        >
      </div>
      <div class="tweet-text">#ProbablyNothing</div>
    </div>
  </div>
</template>

<script>
import tweetsData from "../../tweets.json";

export default {
  data() {
    return {
      tweets: tweetsData,
      filter: "",
    };
  },
};
</script>
