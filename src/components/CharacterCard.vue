<script>
export default {
    props:{
        card: Object
    },
    data(){
        return{
            index: 0
        }
    }
}
</script>

<template lang="">
    <div class="col-12 col-md-3 mt-3">
        <div class="cards-card">
            <div class="card-image">
                <img class="img-fluid" :src="card.card_images[0].image_url" />
            </div>
            <div class="card-info">
                <h4>{{ card.name }}</h4>
                <p>{{ card.type }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
    .cards-card{
        background-color: $primary-color;
        width: 100%;
        height: 100%;
        text-align: center;

        .card-info{
            padding: 5px;


            h4{
                text-transform: uppercase;
                color: $color-white;
                font-size: 15px;
            }
        }

    }
</style>