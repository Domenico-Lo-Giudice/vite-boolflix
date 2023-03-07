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
      return "https://flagsapi.com/" + country + "/flat/64.png";
    },
  },
};
</script>

<template>
  <div v-for="element in this.store.movieOutcome">
    <div class="showCont mx-2">
      <div class="imgShow">
        <img :src="`https://image.tmdb.org/t/p/w342${element.poster_path}`" />
        <div
          class="infoShow d-flex flex-column justify-content-center align-items-center text-center"
        >
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

<style lang="scss">
.imgShow {
  position: relative;
  width: 260px;
  height: 400px;

  img {
    width: 100%;
    height: 100%;
  }
}

.infoShow {
  position: absolute;
  width: 280px;
  height: 400px;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 50%;
  font-size: 30px;
  background-color: black;
  visibility: hidden;
}

.imgShow:hover .infoShow {
  visibility: visible;
}
</style>
