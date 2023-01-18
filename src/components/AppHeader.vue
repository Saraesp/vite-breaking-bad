<script>
export default {
    
}
</script>

<template lang="">
    <Header>
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 mt-2 d-flex">
                    <img src="../assets/image/Yu-Gi-Oh-Logo.jpg" alt="">
                    <h5>Yu-Gi-Oh Api</h5> 
                </div>
            </div>
        </div>
    </Header>
</template>

<style lang="scss">
@use '../style/partials/variables' as *;

    header{
        height: 50px;
        background-color: $color-white;
        position: relative;

        img{
            width: 50px;
            height: 25px;
            margin-top: 5px;
            background-size: cover;
           
        }

        h5{
            position: absolute;
            top: 15px;
            left: 80px;
        }
    }

</style>