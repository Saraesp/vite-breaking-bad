<script>
export default {
    
}
</script>

<template lang="">
    <div class="loader-bg">
        <div class="loader"></div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
    .loader {
        border: 16px solid #f3f3f3; /* Light grey */
        border-top: 16px solid $primary-color; /* Blue */
        border-radius: 50%;
        width: 120px;
        height: 120px;
        position: absolute;
        top: 50%;
        left: 50%;
        animation: spin 2s linear infinite;
}

    .loader-bg{
        background-color: rgba(0, 0, 0, 0.464);
        position: relative;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
}
</style>