<template>
  <div id="app">
    <Header></Header>
    <Calculator></Calculator>
    <Price></Price>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Calculator from './components/Calculator.vue';
import Price from './components/Price.vue';

export default {
  components: {
    Header,
    Calculator,
    Price,
  }
}
</script>

<style>
  @font-face {
    font-family: 'LAB디지털';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_20-07@1.0/LAB디지털.woff') format('woff');
    font-weight: normal;
    font-style: normal;
  }
  body{
    background: #a69fdb;
    font-family: 'LAB디지털';
    color: #fff;
  }
  #app {
    margin-top: 20vh;
  }
</style>