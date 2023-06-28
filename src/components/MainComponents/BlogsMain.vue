<template>
    <article class="hero">
        <div class="my-container">
            <div class="container">
                <div class="row py-5">
                    <div class="col list py-4 px-3">
                        <hgroup>
                            <p class="sup-title">enjoyable sights</p>
                            <h2>Most Viewed <span class="highlight fw-light">Best Blogs</span></h2>
                        </hgroup>

                        <ul class="fa-ul">
                            <li><span class="fa-li"><i class="fa-solid fa-arrow-right-long"></i></span>Become a Better
                                Blogger: Content Planning</li>
                            <li><span class="fa-li"><i class="fa-solid fa-arrow-right-long"></i></span>Promoting Your Online
                                Business on Pinterest</li>
                            <li><span class="fa-li"><i class="fa-solid fa-arrow-right-long"></i></span>Gamification and
                                Game-Based Learning</li>
                            <li><span class="fa-li"><i class="fa-solid fa-arrow-right-long"></i></span>Designing an Online
                                Course from Expert's Perspective</li>
                            <li><span class="fa-li"><i class="fa-solid fa-arrow-right-long"></i></span>Why Online Courses
                                Are the Future of Education</li>
                        </ul>

                    </div>
                    <div class="col card mx-2">
                        <div class="img-card h-50">
                            <img src="../../assets/img/artist-blog-03-480x352.jpeg" alt="artist blog image"
                                class="h-100 w-100">
                        </div>
                        <div class="desc-box">
                            <hgroup class="mb-2">
                                <p class="sup-title grey-text mb-2">Business</p>
                                <h2 class="blog-title">Ten Benefits Of Rentals That May Change Your Perspective</h2>
                            </hgroup>
                            <div class="minor-info">
                                <span class="grey-text me-2"><i class="fa-regular fa-calendar me-1"></i>Dec 28,
                                    2020</span><span class="grey-text"><i class="fa-regular fa-eye me-1"></i>2,260
                                    views</span>
                            </div>
                        </div>
                    </div>
                    <div class="col card">
                        <div class="img-card h-50">
                            <img src="../../assets/img/artist-blog-01-480x352.jpg" alt="artist blog image"
                                class="h-100 w-100">
                        </div>
                        <div class="desc-box">
                            <hgroup class="mb-2">
                                <p class="sup-title grey-text mb-2">Artist</p>
                                <h2 class="blog-title">Pocket-Sized Notebooks Hold Miniature Paintings</h2>
                            </hgroup>
                            <div class="minor-info">
                                <span class="grey-text me-2"><i class="fa-regular fa-calendar me-1"></i>May 15,
                                    2020</span><span class="grey-text"><i class="fa-regular fa-eye me-1"></i>630
                                    views</span>
                            </div>
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

    background-color: $blogHeroColor;
    color: $primaryColor;
    font-weight: bold;

    .card {
        --bs-card-border-radius: 0;
        --bs-card-border-color: 0;

        .img-card {
            overflow: hidden;
        }

    }

    .col.card {
        overflow: hidden;

        hgroup {
            align-items: start;
        }

        .desc-box {
            padding: 1rem .75rem;

            .blog-title {
                font-size: .6rem;
                font-weight: bold
            }

            .minor-info {
                font-size: .5rem;
            }

            h2 {
                cursor: pointer;
            }
        }
    }

    .col.list {
        hgroup {
            align-items: start;

            h2 {
                font-size: 1.3rem;
            }
        }
    }

    ul li {
        font-size: .6rem;

        .fa-li {
            left: -30px;
        }
    }

    ul.fa-ul>li {
        margin-bottom: .8rem;
        cursor: pointer;
        transition: color .5s;
    }

    ul.fa-ul>li:hover {
        color: $primaryHighlight;
    }
}


.img-card img {
    object-fit: cover;
    transition: scale .5s ease-in-out;
}

.img-card:hover img {
    scale: 1.1;
}
</style>