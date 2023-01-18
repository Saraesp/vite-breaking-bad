<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppLoader from './components/AppLoader.vue';
import AppFilter from './components/AppFilter.vue';

import { store } from './store.js';
import axios from 'axios';


export default {
    components: {
      AppHeader,
      AppContent,
      AppLoader,
      AppFilter,
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
        let myUrl = `${store.url}${store.selectedGenere}`;
        console.log(myUrl);

        axios.get(myUrl).then((response) => {
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
    <AppFilter @filter="getAppCard"/>
    <AppContent />
  </div>
  <div v-else>
    <AppLoader />
  </div>
</template>

<style lang="scss">
  @use './style/generals.scss';
</style>