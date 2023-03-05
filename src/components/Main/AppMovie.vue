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
  <div v-for="element in this.store.movieOutcome">
    <div>
      <!-- titolo -->
      {{ element.title }}
    </div>

    <div>
      <!-- titolo originale -->
      {{ element.original_title }}
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
</template>

<style lang="scss"></style>
