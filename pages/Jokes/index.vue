<template>
  <div>
    <SearchJokes v-on:search-text="searchText" />
    <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke" />
  </div>
</template>

<script>

import Joke from "../../components/Joke";
import SearchJokes from "../../components/SearchJokes";

export default defineComponen({
  components: {
    Joke,
    SearchJokes
  },
  data() {
    return {
      jokes: []
    };
  },

  head() {
    return {
      title: "Dad Jokes",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Best place for corny dad jokes"
        }
      ]
    };
  }
});
</script>

<style>
</style>
