<template>
    <article class="hero">
        <div class="my-container">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <h3 class="mb-3">Succesfully trained</h3>
                        <h2 class="highlight my-2">1790</h2>
                        <p class="text-uppercase grey-text">Enrolled learners</p>
                    </div>
                    <div class="col">
                        <h3 class="mb-3">Proudly received</h3>
                        <h2 class="highlight my-2">19</h2>
                        <p class="text-uppercase grey-text">Countrywide Awards</p>
                    </div>
                    <div class="col">
                        <h3 class="mb-3">Firmly established</h3>
                        <h2 class="highlight my-2">24</h2>
                        <p class="text-uppercase grey-text">Local Branches</p>
                    </div>
                    <div class="col">
                        <h3 class="mb-3">Getting featured on</h3>
                        <h2 class="highlight my-2">1090</h2>
                        <p class="text-uppercase grey-text">Blog Posts</p>
                    </div>
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
    background-color: $footerColor;

    .col {
        background-color: #fff;
        border: 1px solid $footerColor;
        padding: 2.5rem .8rem;
        text-align: center;
        font-weight: bold;

        p {
            font-size: .6rem;
        }
    }

    h3 {
        font-size: .8rem;
        text-align: center;
        color: $primaryColor;
        font-weight: bold;

    }
}
</style>