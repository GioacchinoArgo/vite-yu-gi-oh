<script>
import axios from 'axios';
import { store } from './assets/data/store.js';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import AppMain from './components/AppMain.vue'
export default {
  name: 'Yugioh',

  components: { AppHeader, AppFooter, AppMain },
  created() {
    axios.get(endpoint).then(res => {
      store.pokemons = res.data.docs;
    })
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss"></style>
