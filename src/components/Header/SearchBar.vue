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
  <div>
    <form
      action="#"
      @submit.prevent="$emit('search')"
    >
      <input
        type="text"
        v-model="store.userInput"
        placeholder="Search Movie/Tv Series"
      />
      <button type="submit">Ricerca</button>
    </form>
  </div>
</template>

<style lang="scss"></style>
