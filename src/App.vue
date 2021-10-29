<template>
  <div id="app">
    <MainAdvert msg="Welcome to Your Vue.js App"/>
    <Advantages />
    <Guides />
    <TestGuide />
    <Catalogue />
  </div>
</template>

<script>
import MainAdvert from './components/MainAdvert.vue'
import Advantages from './components/Advantages.vue'
import Guides from './components/Guides'
import TestGuide from './components/TestGuide'
import Catalogue from './components/Catalogue'


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
      src: local('Samsung Sans Regular'), url('./assets/samsungFont/SamsungSans-Regular.woff') format('woff');
  }
</style>

<style lang="scss">

body {
  margin: 0;
  padding: 0;

  #app {
    max-width: 1920px;
    margin: 0px auto;
    font-family: 'Samsung Sans Regular';
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
}


</style>
