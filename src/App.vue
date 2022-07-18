<template>
  <div id="app">

    <MainHeader />
    <SeriesPresent />
    <MainFooter />

  </div>
</template>

<script>
import MainHeader from './components/Header.vue';
import SeriesPresent from './components/SeriesPresent.vue';
import MainFooter from './components/Footer.vue';

export default {
  name: 'App',
  components: {

    MainHeader,
    SeriesPresent,
    MainFooter,

  }
}
</script>

<style lang="scss">
@import "./styles/general.scss";

// #app{
//   height: 100vh;
// }

.container {
  width: 1000px;
  margin: 0 auto;
}
</style>
