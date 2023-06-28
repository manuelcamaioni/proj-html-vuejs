<template>
    <header>
        <NavbarApp :navData="navData" />
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
    },
    data() {
        return {
            navData: [
                {
                    link: "Home",
                    content: ["MaxCoach Education", "Course Portal", "Distant learning", "Multimedia Pedagogy", "Modern Schooling", "Remote Training",
                        "Health Coaching", "Gym Coaching", "Business", "Artist", "Kitchen Coach", "Motivation", "Dancing", "Guitar", "Yoga", "Photography", "Personal Finance",
                        "Sales Coaching", "Mental Therapy"],
                },
                {
                    link: "Pages",
                    content: ["Start here", "Success Story", "About me", "About us 01", "About us 02", "About us 03", "Contact me", "Contact us", "Purchase Guide", "Privacy Policy", "Terms of Service"],
                },
                {
                    link: "Courses",
                    content: ["Courses Grid 01", "Courses Grid 02", "Courses Grid 03", "Membership Levels", "Become a Teacher", "Profile", "Checkout", "Single Layout"],
                },
                {
                    link: "Features",
                    content: ["Events", "Zoom Meetings"],
                },
                {
                    link: "Blog",
                    content: ["Blog Grid", "Blog Masonry", "Blog Classic", "Blog List"],
                },
                {
                    link: "Shop",
                    content: ["Shop Left Sidebar", "Shop Right Sidebar", "Cart", "Wishlist", "Single Product"],
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped></style>