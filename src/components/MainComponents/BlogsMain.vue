<template>
    <article class="hero">
        <div class="my-container">
            <div class="container">
                <div class="row">
                    <div class="col">Sezione dei blog</div>
                    <div class="col"></div>
                    <div class="col"></div>
                </div>
            </div>
        </div>
    </article>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

article.hero {
    height: 400px;
    background-color: $BlogHeroColor;
}
</style>