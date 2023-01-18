<script>
import { store } from '../store.js';

export default {
    data(){
        return{
            store,
            archetypes: [
                'Dark Magician',
                'Alien',
                'Laval',
                'Cipher'
            ]
        }
    }
}
</script>

<template lang="">
    <div class="container">
        <div class="row">
            <div class="col-12">
                <div class="mt-5">
                    <select v-model="store.selectedGenere" @change="$emit ('filter')">
                        <option v-for="(item, index) in archetypes" :key="index" :value="item">{{ item }}</option>
                    </select>
                </div>
            </div>
        </div>
        
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

    select{
        background-color: $color-white;
        border: none;
        width: 200px;
        padding: 8px 5px;
        border-radius: 5px;
    }
</style>