<!--
 * @Author: Jiang ShaoDong
 * @Email: jiangshaodong@everimaging.com
 * @Date: 2021-02-26 11:40:20
 * @Description: 
-->
<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

import {Chart} from 'chart.js';
// let Chart = require('chart.js')
window['myChart'] = Chart
// import helpers from 'chart.js/helpers'
// Chart.helpers = helpers
import ChartDataLabels from 'chartjs-plugin-datalabels/dist/chartjs-plugin-datalabels';


Chart.plugins.register(ChartDataLabels);

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
