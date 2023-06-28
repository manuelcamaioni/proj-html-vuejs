<template>
    <article class="hero">
        <div class="my-container">
            <hgroup class="mb-4">
                <p class="sup-title">Great Words about MaxCoach</p>
                <h2 class="fs-3 fw-bold">Our <span class="highlight fw-light">top learners'</span> verbatim</h2>
            </hgroup>
            <div class="carousel d-flex position-relative mb-3">
                <button class="btn btn-left position-absolute" @click="prevButton"><i
                        class="fa-solid fa-chevron-left"></i></button>
                <div class="card w-50 d-flex flex-column justify-content-around" v-for="(card, index) in cards"
                    :class="activeIndex === index ? '' : 'd-none'">
                    <div class="about-box mb-">
                        <h5>{{ card.title }}</h5>
                        <p>{{ card.info }}</p>
                    </div>
                    <div class="client-box d-flex">
                        <img :src="getImagePath(card.path)" :alt="card.path">
                        <div class="info">
                            <p class="name text-uppercase">{{ card.name }}</p>
                            <p class="position">{{ card.position }}</p>
                        </div>
                    </div>
                </div>
                <button class="btn btn-right position-absolute" @click="nextButton"><i
                        class="fa-solid fa-chevron-right"></i></button>

            </div>
            <div class="dots-miniature d-flex justify-content-center mb-5">
                <i v-for="(dot, index) in cards" class="fa-solid fa-circle"
                    :class="activeIndex === index ? 'opacity-100' : ''"></i>
            </div>
            <div class="certification-box text-center">
                <h5 class="fs-6 mb-0 fw-bold">Start Today for getting <span class="highlight fw-light">Online
                        Certification</span>
                </h5>
                <h4 class="fs-5 fw-bold mb-4">You can be your own guiding star with out help!</h4>
                <button class="btn custom_btn fw-bold">Get started now</button>
            </div>
        </div>
    </article>
</template>

<script>

export default {
    methods: {
        getImagePath: function (img) {
            return new URL(`../../assets/img/${img}`, import.meta.url).href;
        },

        nextButton: function () {
            if (this.activeIndex === this.cards.length - 1) this.activeIndex = 0;
            else this.activeIndex += 1;
        },
        prevButton: function () {
            if (this.activeIndex === 0) this.activeIndex = this.cards.length - 1;
            else this.activeIndex -= 1;
        },
    },
    data() {
        return {
            activeIndex: 0,
            cards: [
                {
                    title: "High Level of efficiency and scientific teaching methods",
                    info: "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
                    path: "testimonial-avata-02.jpg",
                    name: "Mina Hollace",
                    position: "/ Freelancer",
                },
                {
                    title: "Professional team of specialists and passionate mentors at reach",
                    info: "I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and profesional when dealing with students.",
                    path: "testimonial-avata-04.jpg",
                    name: "Madley Podor",
                    position: "/ IT Specialist",
                },
                {
                    title: "The MaxCoach team works really hard to ensure high quality",
                    info: "I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation into effective methods to be adopted for learners of all levels.",
                    path: "testimonial-avata-01.jpg",
                    name: "Luvic Dubble",
                    position: "/ Private Tutor",
                },
                {
                    title: "It's a choice of quality for people with special needs",
                    info: "I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.",
                    path: "testimonial-avata-03.jpg",
                    name: "Florence Themes",
                    position: "/ Multimedia Admin",
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

article.hero {

    background-color: $footerColor;

    .my-container {
        padding: 2.5rem 0;
    }

    .card {
        margin: 0 auto;
        --bs-card-border-color: none;
        padding: 2rem;
        height: 300px;

        h5 {
            font-size: .8rem;
            color: $primaryColor;
            font-weight: bold;

        }

        p {
            color: $secondaryTextColor;
            font-size: .65rem;
            font-weight: bold;
        }

        .client-box {
            img {
                width: 50px;
                height: 50px;
                border-radius: 50%;
                margin-right: .5rem;
            }

            .name {
                margin: .2rem 0;
                color: $primaryColor;
                font-weight: bold;
                font-size: .7rem;
            }

            .position {
                font-size: .6rem;
                margin-bottom: .2rem;
            }
        }
    }

    .btn-left,
    .btn-right {
        background-color: transparent;
    }

    .btn-left {
        top: 50%;
        transform: translateY(-50%);
    }

    .btn-right {
        right: 0;
        top: 50%;
        transform: translateY(-50%);
    }

    .dots-miniature {
        padding: 1rem 0;

        i {
            font-size: .3rem;
            margin: 0 .5rem;
            opacity: 0.5;
        }
    }

    .certification-box {

        color: $primaryColor;

        .btn {
            background-color: $primaryHighlight;
            color: white;
            font-size: .6rem;
        }

        .custom_btn:hover {
            background-color: $primaryColor;
        }
    }

}
</style>