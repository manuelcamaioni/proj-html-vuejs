<template>
    <header>
        <NavbarApp />
        <HeaderHero />
    </header>
</template>

<script>
import NavbarApp from "./HeaderComponents/NavbarApp.vue";
import HeaderHero from "./HeaderComponents/HeaderHero.vue";

export default {
    components: {
        NavbarApp, HeaderHero
    }
}
</script>

<style lang="scss" scoped></style>