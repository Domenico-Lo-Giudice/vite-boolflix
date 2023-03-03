<script>
import AppHeader from "./components/Header/AppHeader.vue";
import AppMain from "./components/Main/AppMain.vue";
import axios from "axios";
import { store } from "./store.js";

export default {
  data() {
    return {
      store,
    };
  },
  created() {},
  methods: {},
  components: {
    AppHeader,
    AppMain,
  },
};
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main>
    <AppMain />
  </main>
</template>

<style lang="scss"></style>
