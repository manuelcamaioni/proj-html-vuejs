<template>
    <header>
        <NavbarApp />
        <HeaderHero />
        <HeaderBrands />
    </header>
</template>

<script>
import NavbarApp from "./HeaderComponents/NavbarApp.vue";
import HeaderHero from "./HeaderComponents/HeaderHero.vue";
import HeaderBrands from "./HeaderComponents/HeaderBrands.vue";

export default {
    components: {
        NavbarApp, HeaderHero, HeaderBrands,
    }
}
</script>

<style lang="scss" scoped></style>