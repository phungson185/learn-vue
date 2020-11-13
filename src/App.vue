<template>
  <div id="app">
    <brgSun />
    <headerPage />
    <sunPage />
    <footerPage />
  </div>
</template>

<script>
import sunPage from './components/sunPage.vue'
import headerPage from './components/headerPage.vue'
import footerPage from './components/footerPage.vue'
import brgSun from './components/background.vue'

export default {
  name: 'App',
  components: {
    headerPage,
    sunPage,
    footerPage,
    brgSun
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    margin: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #fff;
    font-size: 15px;
    line-height:  1.5;
    width: 100%;
    background-color: gainsboro;
}
</style>
