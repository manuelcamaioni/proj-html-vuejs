<template>
    <article class="hero">
        <div class="my-container d-flex">
            <div class="video-container">
                <img src="../../assets/img/home-2-popup-video-poster.jpg" alt="thumbnail's video">
                <img src="../../assets/img/icon-youtube-play.png" alt="youtube icon" class="over-icon">
            </div>
            <div class="info-box">

                <span class="text-uppercase">Get started effrotlessly</span>
                <h2>Enjoy Our <span>Companionship</span></h2>
                <p>Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for some
                    hidden hints of early-bird rewards as well.</p>
                <a href="#">Download free guide book &#8594</a>

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
    .video-container {
        width: 50%;
        overflow: hidden;
        border-radius: 0.3rem;
        position: relative;

        .over-icon {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 60px;
        }

        img {
            width: 100%;
            border-radius: 0.3rem;
        }

    }

    .info-box {
        width: 50%;
    }
}
</style>