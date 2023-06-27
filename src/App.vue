<template>
  <HeaderApp />
  <MainApp />
  <FooterApp />
</template>

<script>
import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";

export default {
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
  },
  data() {
    return {

    }
  },
}
</script>

<style lang="scss">
@import "bootstrap/scss/bootstrap";
@import "./styles/general.scss";
@import url('https://fonts.cdnfonts.com/css/gilroy-bold');
@import url('https://fonts.cdnfonts.com/css/gilroy-heavy');
@import url('https://fonts.cdnfonts.com/css/gilroy-light');
@import url('https://fonts.cdnfonts.com/css/gilroy-medium');
</style>
