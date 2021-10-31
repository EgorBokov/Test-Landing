<template>
  <div id="app">
    <MainAdvert /> 
    <Advantages />
    <Guides />
    <TestGuide /> 
    <Catalogue />
  </div>
</template>

<script>
import MainAdvert from './components/main-components/MainAdvert.vue'
import Advantages from './components/main-components/Advantages.vue'
import Guides from './components/main-components/Guides.vue'
import TestGuide from './components/main-components/TestGuide.vue'
import Catalogue from './components/main-components/Catalogue.vue'


export default {
  name: 'App',
  components: {
    MainAdvert,
    Advantages,
    Guides,
    TestGuide,
    Catalogue,
  }
}
</script>

<style>
  @font-face {
      font-family: 'Samsung Sans Regular';
      font-style: normal;
      font-weight: normal;
      src: local('Samsung Sans Regular'), url('./assets/fonts/samsung-font/SamsungSans-Regular.woff') format('woff');
  }
</style>

<style lang="scss">

$main-color: #1D1D20;


body {
  margin: 0;
  padding: 0;

  #app {
    margin: 0px auto;
    font-family: 'Samsung Sans Regular';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: $main-color;
  }
}


</style>
