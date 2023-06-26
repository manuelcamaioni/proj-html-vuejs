<template>
    <main>
        <CoursesMain />
        <TutoringMain />
    </main>
</template>

<script>
import CoursesMain from "./MainComponents/CoursesMain.vue";
import TutoringMain from "./MainComponents/TutoringMain.vue";
export default {
    components: {
        CoursesMain, TutoringMain
    }
}
</script>

<style lang="scss" scoped></style>