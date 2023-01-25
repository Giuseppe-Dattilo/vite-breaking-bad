<script>
import SelectForm from './components/SelectForm.vue';
import axios from 'axios';
import { store } from './data/store';
import AppMain from './components/AppMain.vue'
export default {
  components: { AppMain, SelectForm },
  data() {
    return {
      store
    }
  },
  methods: {
    fetchcharacters(url) {
      axios.get(url)
        .then(res => {
          store.characters = res.data.docs;
        });
    }
  },
  created() {
    this.fetchcharacters('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=10&page=10');
  }
};
</script>

<template>
  <header>
    <h1 class="text-center my-5 text-white fw-bold">Pokemon</h1>
  </header>
  <select-form></select-form>
  <app-main></app-main>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>
