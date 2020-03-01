<template>
  <div id="app">
    <div class="container">
      <a href="#filesHeader" class="side-link-left">ФАЙЛЫ</a>
      <div class="content-wrapper">
        <Header />
        <MainContent />
        <Footer />
      </div>
      <a href="#locationHeader" class="side-link-right">МЕСТОПОЛОЖЕНИЕ</a>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import MainContent from "./components/MainContent.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    MainContent
  }
};
</script>

<style lang="scss">
@import "./assets/scss/main.scss";
</style>
