<script>
import SearchBar from "./SearchBar.vue";
import axios from "axios";
import { store } from "../../store";

export default {
  data() {
    return {
      store,
    };
  },

  created() {},
  methods: {
    getMovie() {
      axios
        .get(
          "https://api.themoviedb.org/3/search/movie?api_key=3ddad31363e335e702734af33371ae8b&query=" +
            this.store.userInput
        )
        .then((response) => {
          this.store.movieOutcome = response.data.results;
        });
      axios
        .get(
          "https://api.themoviedb.org/3/search/tv?api_key=3ddad31363e335e702734af33371ae8b&query=" +
            this.store.userInput
        )
        .then((response) => {
          this.store.seriesOutcome = response.data.results;
        });
    },
  },
  components: { SearchBar },
};
</script>

<template>
  <header>
    <div
      class="container-fluid bg-dark d-flex justify-content-between align-items-center"
    >
      <div>
        <h1 class="">Boolflix</h1>
      </div>
      <SearchBar @search="getMovie" />
    </div>
  </header>
</template>

<style lang="scss">
header > div {
  height: 150px;
  h1 {
    color: red;
  }
}
</style>
