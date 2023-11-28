<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import { store } from "./store.js";
import CharactersList from "./components/CharactersList.vue";
import AppSelect from "./components/AppSelect.vue";

export default {
  data() {
    return {
      store,
    };
  },
  created() {
    this.createCards()
  },
  components: { AppHeader, CharactersList, AppSelect },
  methods: {
    createCards() {
      axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0").then((resp) => {
        this.store.cards = resp.data.data;
      });
    },
    handleSearch() {
      if (this.store.selectCards.length > 0) {
        axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0", {
          params: {
            archetype: this.store.selectCards,
          }
        }).then((resp) => {
          this.store.cards = resp.data.data;
        })
      } else {
        this.createCards()
      }

    }
  }
};
</script>

<template>
  <AppHeader />
  <AppSelect @cardSelect="handleSearch" />
  <CharactersList />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>
