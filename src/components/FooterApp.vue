<template>
    <footer>
        <NewsletterFooter />
        <InfoFooter :addressData="addressData" />
    </footer>
</template>

<script>
import NewsletterFooter from "./FooterComponents/NewsletterFooter.vue";
import InfoFooter from "./FooterComponents/InfoFooter.vue";
export default {
    components: {
        NewsletterFooter, InfoFooter
    },
    data() {
        return {
            addressData: {
                address: "382 NE 191st St # 87394 Miami, FL 33179-3899",
                phone: "+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)",
                email: "support@maxcoach.com"
            }
        }
    },
}
</script>

<style lang="scss" scoped>
@use "../styles/variables.scss" as *;

footer {
    background-color: $footerColor;
}
</style>