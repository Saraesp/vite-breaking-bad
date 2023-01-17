<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';

import { store } from './store.js';
import axios from 'axios';


export default {
    components: {
      AppHeader,
      AppContent,
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
        })
      }
    },
}
</script>

<template lang="">
        <AppHeader />
        <AppContent />
</template>

<style lang="scss">
  @use './style/generals.scss';
</style>