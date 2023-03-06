<script>
import { store } from "../../store";
export default {
  data() {
    return {
      store,
    };
  },
  created() {},
  methods: {},
};
</script>

<template>
  <div v-for="element in this.store.seriesOutcome">
    <div class="showCont mx-2">
      <div class="imgShow">
        <img :src="`https://image.tmdb.org/t/p/w342${element.poster_path}`" />
        <div
          class="infoShow d-flex flex-column justify-content-center align-items-center text-center"
        >
          <div>
            <!-- titolo -->
            {{ element.name }}
          </div>

          <div>
            <!-- titolo originale -->
            {{ element.original_name }}
          </div>

          <div>
            <!-- lingua -->
            {{ element.original_language }}
          </div>

          <div>
            <!-- valutazione -->
            {{ element.vote_average }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss"></style>
