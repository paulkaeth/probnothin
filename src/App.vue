<template>
  <div id="app" class="app w-full max-w-full">
    <Header />
    <Hero />
    <Filters :filterTweets="filterTweets" />
    <Tweets :tweets="tweets" />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Filters from "./components/Filters.vue";
import Tweets from "./components/Tweets.vue";
import Footer from "./components/Footer.vue";

import tweetsData from "./tweets.json";

export default {
  name: "App",
  components: {
    Header,
    Hero,
    Filters,
    Tweets,
    Footer,
  },
  data() {
    return {
      tweets: tweetsData,
    };
  },
  methods: {
    filterTweets(catName) {
      this.tweets = tweetsData;
      if (catName !== "All") {
        this.tweets = this.tweets.filter((tweet) => {
          return tweet.category === catName;
        });
      }
    },
  },
};
</script>
