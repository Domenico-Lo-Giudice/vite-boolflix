<script>
import { store } from "../../store";
import AppMovie from "./AppMovie.vue";
import AppTvSeries from "./AppTvSeries.vue";
export default {
  data() {
    return {
      store,
    };
  },
  created() {},
  methods: {},
  components: {
    AppMovie,
    AppTvSeries,
  },
};
</script>

<template>
  <div>
    <AppMovie />
    <AppTvSeries />
  </div>
</template>

<style lang="scss"></style>
