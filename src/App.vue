<template>
  <div id="app">
    <Header></Header>
    <Calculator @showResult="showPrice"></Calculator>
    <Price :showResult='resultPrice'></Price>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Calculator from './components/Calculator.vue';
import Price from './components/Price.vue';

export default {
  data () {
    return {
      resultPrice: 0
    }
  },
  components: {
    Header,
    Calculator,
    Price,
  },
  methods: {
    showPrice(price,people) {
      // console.log(Math.round(price/people));
      this.resultPrice = Math.round(price/people);
    }
  },
  
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
        text-shadow: -1px -1px 0px #666;
  }
  #app {
    margin-top: 20vh;
  }
</style>