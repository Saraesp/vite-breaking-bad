<script>
import CharacterCard from './CharacterCard.vue'
import { store } from '../store.js';

export default {
    components:{
        CharacterCard
    },
    data(){
       return{
            store  
    } 
    }
}
</script>

<template lang="">
    <main class="container">
        <div class="row">
            Carte trovate: {{ store.cardList.length }}
        </div>
        <div class="row">
            <CharacterCard v-for="(item, index) in store.cardList" :key="index" :card="item" />
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

    main{
        background-color: $color-white;
        margin-top: 4rem;
    }
</style>