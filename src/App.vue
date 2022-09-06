<template>
  <div id="app">
    <NavHeader/>
    <MainContent/>
    <FooterComponent/>
  </div>
</template>

<script>
import NavHeader from './components/NavHeader.vue';
import MainContent from './components/MainContent.vue';
import FooterComponent from './FooterComponent.vue';

export default {
  name: 'App',
  components: {
    NavHeader,
    MainContent,
    FooterComponent
}
}
</script>

<style lang="scss">
  @import './style/general.scss';
</style>
