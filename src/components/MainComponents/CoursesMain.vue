<template>
    <article class="hero">
        <div class="my-container h-100">
            <hgroup>
                <p>Stimulated to learn?</p>
                <h1>Featured Online Courses</h1>
            </hgroup>
            <div class="courses-list">
                <ul class="w-100 d-flex flex-wrap">
                    <li class="course"></li>
                    <li class="course"></li>
                    <li class="course"></li>
                    <li class="course"></li>
                    <li class="course"></li>
                    <li class="course"></li>
                </ul>
            </div>
        </div>
    </article>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
article.hero {

    border: 1px solid orange;

    hgroup {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    div.courses-list {
        width: 100%;

        li.course {
            width: calc(100% / 2);
            height: 60px;
            border: 1px solid red;
        }
    }
}
</style>