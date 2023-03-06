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
        class="input"
        type="text"
        v-model="store.userInput"
        placeholder="Search Movie/Tv Series"
      />
      <button
        type="submit"
        class="button ms-1"
      >
        Ricerca
      </button>
    </form>
  </div>
</template>

<style lang="scss">
.input {
  border-color: black;
  border-radius: 10px;
}

.button {
  border-radius: 10px;
  padding: 1px 5px;
  border-color: black;
}
button:hover {
  color: red;
}

.button:active {
  background-color: #3e828e;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
</style>
