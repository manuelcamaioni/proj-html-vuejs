<template>
    <article class="hero">
        <div class="my-container h-100">
            <hgroup>
                <p class="sup-title">MaxCoach available courses</p>
                <h2 class="fs-3 fw-bold">Access <span class="highlight fw-light">Smart Tutoring</span> Program For Benefits.
                </h2>
            </hgroup>
            <div class="container">
                <div class="row">
                    <div class="col">
                        <div class="img-container">
                            <img src="../../assets/img/home-2-image-box-01.png" alt="">
                        </div>
                        <div class="desc-box">
                            <h3>Customize Preferences</h3>
                            <p class="xs-text">Learners are given the right to arrange and customize their study
                                schedule and timetable
                                based on preferences.</p>
                            <a href="#" class="fw-bold">Start here <i class="fa-solid fa-arrow-right"></i></a>
                        </div>
                    </div>
                    <div class="col">
                        <div class="img-container">
                            <img src="../../assets/img/about-us-02-image-box-02.png" alt="">
                        </div>
                        <div class="desc-box">
                            <h3>Cloud Storage</h3>
                            <p class="xs-text">You can store online lessons via online cloud or download to your
                                device and revise lessons
                                on the way.</p>
                            <a href="#" class="fw-bold">Get Free quote <i class="fa-solid fa-arrow-right"></i></a>
                        </div>
                    </div>
                    <div class="col">
                        <div class="img-container">
                            <img src="../../assets/img/home-2-image-box-03.png" alt="#">
                        </div>
                        <div class="desc-box">
                            <h3>Multimedia Channels</h3>
                            <p class="xs-text">We provide study materials with various formats: video, audio,
                                slides, doc, prints, books and
                                applications.</p>
                            <a href="#" class="fw-bold">Start now <i class="fa-solid fa-arrow-right"></i></a>
                        </div>
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


    h3 {
        color: $primaryColor;
        font-size: 1rem;
        font-weight: bolder;
    }

    p,
    a {
        color: $secondaryTextColor;
        text-decoration: none;
    }

    a {
        font-size: .55rem;
    }

}
</style>