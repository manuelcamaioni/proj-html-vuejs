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
</style>
