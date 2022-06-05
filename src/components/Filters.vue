<template>
  <div class="block md:max-w-screen-xl lg:max-w-screen-2xl md:mx-auto mb-12 md:mb-24 px-6 text-center">
    <span v-for="filter in filters" :key="filter" @click="() => filterTweets(filter)" class="cursor-pointer text-slate-100 hover:text-blue-500 px-3">
      {{ filter }}
    </span>
  </div>
</template>

<script>
const filters = ["All", "OpenDAO", "SOS", "721", "SOSMarket"];

export default {
  props: ["filterTweets"],

  data() {
    return {
      filters,
    };
  },
};
</script>
