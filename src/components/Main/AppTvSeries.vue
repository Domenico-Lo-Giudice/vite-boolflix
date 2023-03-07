<script>
import { store } from "../../store";
export default {
  data() {
    return {
      store,
    };
  },
  created() {},
  methods: {
    getFlag(country) {
      country = country.toUpperCase();

      if (country == "EN") return "https://flagsapi.com/GB/flat/64.png";
      if (country == "CS") return "https://flagsapi.com/GB/flat/64.png";
      if (country == "HI") return "https://flagsapi.com/GB/flat/64.png";
      if (country == "JA") return "https://flagsapi.com/JP/flat/64.png";
      if (country == "KO") return "https://flagsapi.com/KR/flat/64.png";
      if (country == "ZH") return "https://flagsapi.com/CN/flat/64.png";
      return "https://flagsapi.com/" + country + "/flat/64.png";
    },
  },
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
            <img :src="getFlag(element.original_language)" />
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
