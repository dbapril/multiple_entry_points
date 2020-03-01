<template>
  <div id="app">
    <div class="container">
      <div class="content-wrapper">
        <Header />
        <FormMainContent />
        <Footer class="form-footer" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import FormMainContent from "./components/FormMainContent.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "Form",
  components: {
    Header,
    FormMainContent,
    Footer
  }
};
</script>

<style lang="scss">
@import "./assets/scss/main.scss";
</style>
