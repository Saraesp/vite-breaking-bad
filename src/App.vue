<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';

export default {
    components: {
      AppHeader,
      AppContent,
    }
}
</script>

<template lang="">
        <AppHeader />
        <AppContent />
</template>

<style lang="scss">
  @use './style/generals.scss';
</style>