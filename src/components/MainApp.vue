<template>
    <main>
        <CoursesMain />
        <TutoringMain />
        <TrailerMain />
    </main>
</template>

<script>
import CoursesMain from "./MainComponents/CoursesMain.vue";
import TutoringMain from "./MainComponents/TutoringMain.vue";
import TrailerMain from "./MainComponents/TrailerMain.vue";
export default {
    components: {
        CoursesMain, TutoringMain, TrailerMain
    }
}
</script>

<style lang="scss" scoped></style>