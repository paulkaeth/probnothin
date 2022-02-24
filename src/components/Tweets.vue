<template>
  <section class="md:max-w-screen-xl lg:max-w-screen-2xl md:mx-auto px-6">
    <div class="grid gap-4 lg:gap-8 grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
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
              href="https://twitter.com/intent/tweet?text=Hello World"
              >Tweet me</a
            >
          </div>
          <div class="tweet-text">#ProbablyNothing</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: ["tweets"],
};
</script>
