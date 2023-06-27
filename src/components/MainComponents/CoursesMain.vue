<template>
    <article class="hero ">
        <div class="my-container py-3">
            <hgroup>
                <p class="sup-title">Stimulated to learn?</p>
                <h1 class="fs-3 mb-2">Featured Online Courses</h1>
            </hgroup>
            <div class="courses-list">
                <ul class="w-100 d-flex flex-wrap">
                    <li class="course  px-1 mb-3" v-for="course in courses">
                        <div class="img-box">
                            <img :src="getImagePath(course.path)" :alt="course.type">
                        </div>
                        <div class="desc-box ps-1">
                            <h4>
                                <span v-if="(typeof course.price === 'number')">&#36;</span>{{ course.price }}<span
                                    v-if="(typeof course.price === 'number')" class="xs-text">.00</span>
                            </h4>
                            <h5>{{ course.type }}</h5>
                            <div class="other-info grey-text d-flex justify-content-evenly pe-4">
                                <span><i class="fa-solid fa-file-lines me-1"></i>{{ course.lessons }} Lessons</span>
                                <span><i class="fa-regular fa-user me-1"></i>{{ course.students }} Students</span>
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="d-flex justify-content-center">
                <button class="btn custom_btn">
                    <span class="fw-bold">View all courses <i class="fa-solid fa-arrow-right"></i></span>
                </button>
            </div>
        </div>
    </article>
</template>

<script>
export default {
    data() {
        return {
            courses: [
                {
                    path: "course-01.jpg",
                    price: "Free",
                    type: "Personal Finance: Financial Security Thinking & Principles",
                    lessons: 2,
                    students: 260,
                },
                {
                    path: "course-02.jpg",
                    price: 40,
                    type: "Learning to Write as a Professional Author",
                    lessons: 20,
                    students: 69,
                },
                {
                    path: "course-03.jpg",
                    price: "Free",
                    type: "Customer-centric Info-Tech Strategies",
                    lessons: 24,
                    students: 927,
                },
                {
                    path: "course-04.jpg",
                    price: 19,
                    type: "Open Programming Courses for Everyone: Python",
                    lessons: 17,
                    students: 66,
                },
                {
                    path: "course-05.jpg",
                    price: 26,
                    type: "Academic Listening and Note-taking",
                    lessons: 14,
                    students: 68,
                },
                {
                    path: "course-06.jpg",
                    price: 39,
                    type: "Master jQuery in a Short Period of Time",
                    lessons: 6,
                    students: 51,
                },
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../../assets/img/${img}`, import.meta.url).href;
        }
    },
    mounted() {

        console.log(typeof this.courses[1].price);
    }

}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

article.hero {
    background-color: $secondaryHeroColor;
}

.custom_btn {
    background-color: $primaryHighlight;
    color: white;
    margin: 1rem 0;

    span {
        font-size: .6rem;
        font-weight: bolder;
    }

}

div.courses-list {
    width: 100%;

    li.course {
        width: calc(100% / 2);
        display: flex;
        flex-wrap: wrap;

        .img-box {
            width: 100px;


            img {
                width: 80px;
                height: 80px;
                object-fit: cover;

                border-radius: 50%;
            }
        }

        .desc-box {
            width: calc(100% - 100px);
            display: flex;
            flex-direction: column;
            justify-content: center;

            h4 {
                font-size: .9rem;
                margin: 0;
                color: $primaryHighlight;
            }

            h5 {
                font-size: .8rem;
                margin-bottom: .4rem;
                color: $primaryColor;
            }

            .other-info {
                font-size: .65rem;
            }
        }
    }
}
</style>