<template>
    <article class="hero">
        <div class="my-container d-flex justify-content-between">
            <div class="video-container d-flex align-items-center">
                <img src="../../assets/img/home-2-popup-video-poster.jpg" alt="thumbnail's video" class="thumbnail">
                <img src="../../assets/img/icon-youtube-play.png" alt="youtube icon" class="over-icon">
            </div>
            <div class="info-box">

                <h6 class="text-uppercase">Get started <span class="highlight">effortlessly</span></h6>
                <h2>Enjoy Our <span class="highlight">Companionship</span></h2>
                <p class="grey-text">Sneek peek into what has in store for you on our online teaching and mentoring portal.
                    Seek for some
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
    color: $primaryColor;

    .video-container {
        width: 50%;
        height: 300px;
        overflow: hidden;
        border-radius: 0.3rem;
        position: relative;

        .over-icon {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 40px;
        }

        img.thumbnail {
            width: 100%;
            border-radius: 0.3rem;
        }

    }

    .info-box {
        width: 45%;
        padding-top: 3rem;
        padding-right: 1rem;

        h6 {
            font-size: .7rem;
        }

        h2 {
            font-size: 1.5rem;
            font-weight: bold;
        }

        p {
            font-size: .8rem;
        }

        a {
            color: $primaryHighlight;
            text-decoration: none;
            font-weight: bold;
            font-size: .7rem;
        }
    }
}
</style>