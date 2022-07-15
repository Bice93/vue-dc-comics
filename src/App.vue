<template>
  <div id="app">

    <MainHeader />
    <MainMain />
    <MainFooter />

  </div>
</template>

<script>
import MainHeader from './components/Header.vue';
import MainMain from './components/Main.vue';
import MainFooter from './components/Footer.vue';

export default {
  name: 'App',
  components: {

    MainHeader,
    MainMain,
    MainFooter,
    
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
