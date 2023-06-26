<template>
    <footer>
        <NewsletterFooter />
        <InfoFooter />
    </footer>
</template>

<script>
import NewsletterFooter from "./FooterComponents/NewsletterFooter.vue";
import InfoFooter from "./FooterComponents/InfoFooter.vue";
export default {
    components: {
        NewsletterFooter, InfoFooter
    }
}
</script>

<style lang="scss" scoped></style>