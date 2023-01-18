<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppLoader from './components/AppLoader.vue';

import { store } from './store.js';
import axios from 'axios';


export default {
    components: {
      AppHeader,
      AppContent,
      AppLoader
    },
    data(){
      return {
        store
      }
    },
    created() {
      this.getAppCard();
    },
    methods: {
      getAppCard(){
        axios.get(store.url).then((response) => {
          store.cardList = response.data.data;
          setTimeout(() => {
            store.isLoader = true
          }, 3000)
        })
      }
    },
}
</script>

<template lang="">
  <div v-if="store.isLoader">
    <AppHeader />
    <AppContent />
  </div>
  <div v-else>
    <AppLoader />
  </div>
</template>

<style lang="scss">
  @use './style/generals.scss';
</style>