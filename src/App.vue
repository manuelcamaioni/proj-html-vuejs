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
@import url('https://fonts.googleapis.com/css2?family=Cabin:wght@400;500;600;700&family=Fira+Sans:ital,wght@0,500;0,600;1,400;1,500&family=Montserrat:wght@300;500;700&family=Open+Sans:ital,wght@0,300;0,700;0,800;1,500&family=PT+Sans:ital,wght@0,700;1,400&display=swap');
</style>
