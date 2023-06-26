<template>
    <main>
        <CoursesMain />
        <TutoringMain />
        <TrailerMain />
        <TopLearners />
        <StatsMain />
        <BlogsMain />
    </main>
</template>

<script>
import CoursesMain from "./MainComponents/CoursesMain.vue";
import TutoringMain from "./MainComponents/TutoringMain.vue";
import TrailerMain from "./MainComponents/TrailerMain.vue";
import TopLearners from "./MainComponents/TopLearnersMain.vue";
import StatsMain from "./MainComponents/StatsMain.vue";
import BlogsMain from "./MainComponents/BlogsMain.vue";
export default {
    components: {
        CoursesMain, TutoringMain, TrailerMain, TopLearners, StatsMain, BlogsMain
    }
}
</script>

<style lang="scss" scoped></style>