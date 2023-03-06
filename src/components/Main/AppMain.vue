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
  <div class="mainCont px-2">
    <div>
      <h4 class="title px-3">Movies</h4>
    </div>

    <div
      class="moviesTvSeries d-flex align-items-center justify-content-between"
    >
      <AppMovie />
    </div>

    <div>
      <h4 class="px-3">Tv Series</h4>
    </div>

    <div class="TvSeries d-flex align-items-center justify-content-between">
      <AppTvSeries />
    </div>
  </div>
</template>

<style lang="scss">
.mainCont {
  padding-top: 50px;
  background-color: #2c2c2c;
  color: white;
}

.moviesTvSeries,
.TvSeries {
  overflow: auto;
  width: 100%;
  height: 700px;
  margin-top: -100px;
}
</style>
