<template>
  <div id="app">
    <NavHeader/>
  </div>
</template>

<script>
import NavHeader from './components/NavHeader.vue';

export default {
  name: 'App',
  components: {
    NavHeader
}
}
</script>

<style lang="scss">
  @import './style/general.scss';
</style>
