<template>
    <div class="hero">
        <div class="my-container">
            <div class="container">
                <div class="row">
                    <div class="col-5 d-flex flex-column justify-content-center">
                        <hgroup>
                            <h1 class="fs-2">
                                Distant learning for further expansion
                            </h1>
                            <p class="minor-text">
                                Learning is a life-long journey that in fact we never find that terminate stop. Stop
                                searching,
                                enjoy the process.
                            </p>
                        </hgroup>
                        <div class="download-btn">
                            <button class="btn custom_btn">
                                <i class="fa-solid fa-download fa-sm"></i> <span>Download free guide</span>
                            </button>
                        </div>
                        <span class="minor-text question-box">Have Questions? <a href="#">Get Free Samples <i
                                    class="fa-solid fa-arrow-right"></i></a>
                        </span>
                    </div>
                    <div class="col-7 profile-pic-container">
                        <img src="../../assets/img/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg"
                            alt="Girl's image profile">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;


div.hero {
    h1 {
        color: $primaryColor;
    }

    div.col-5,
    div.col-7 {
        padding: 0;
    }

    .custom_btn {
        background-color: $primaryHighlight;
        color: white;
    }

    .profile-pic-container {
        img {
            width: 100%;
            border-radius: 50%;

        }
    }

    span.question-box {
        font-size: .7rem;

        a {
            color: $primaryHighlight;

        }
    }
}
</style>