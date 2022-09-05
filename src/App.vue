<template>
  <div id="app">
    <NavHeader/>
    <MainContent/>
  </div>
</template>

<script>
import NavHeader from './components/NavHeader.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  components: {
    NavHeader,
    MainContent
}
}
</script>

<style lang="scss">
  @import './style/general.scss';
</style>
