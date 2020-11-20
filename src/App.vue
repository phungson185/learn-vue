<template>
  <div id="app">
    <brgSun />
    <headerPage v-on:changeTabHeader="updateParent"/>
    <sunPage v-if="isChoice === 'SUN'"/>
    <votePage v-else-if="isChoice ==='Vote'"/>
    <faqsPage v-else-if="isChoice ==='FAQs'"/>
    <footerPage />
  </div>
</template>

<script>
import sunPage from './components/sunPage.vue'
import headerPage from './components/headerPage.vue'
import brgSun from './components/background.vue'
import faqsPage from './components/faqsPage.vue'
import votePage from './components/votePage.vue'
import footerPage from './components/footerPage.vue'

export default {
  name: 'App',
  components: {
    headerPage,
    sunPage,
    brgSun,
    faqsPage,
    votePage,
    footerPage
  },
  methods: {
    updateParent(value) {
        this.isChoice = value;
    }
  },
  data() {
    return {
      isChoice: "SUN",
    }
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

a{
  text-decoration: none;
}

li {
  list-style: none;
}
</style>
