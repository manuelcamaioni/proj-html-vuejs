<template>
    <main>
        <CoursesMain />
        <TutoringMain />
        <TrailerMain />
        <TopLearners />
    </main>
</template>

<script>
import CoursesMain from "./MainComponents/CoursesMain.vue";
import TutoringMain from "./MainComponents/TutoringMain.vue";
import TrailerMain from "./MainComponents/TrailerMain.vue";
import TopLearners from "./MainComponents/TopLearnersMain.vue"
export default {
    components: {
        CoursesMain, TutoringMain, TrailerMain, TopLearners
    }
}
</script>

<style lang="scss" scoped></style>