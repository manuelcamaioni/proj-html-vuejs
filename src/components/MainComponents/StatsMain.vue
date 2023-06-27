<template>
    <article class="hero" ref="elementToWatch">
        <div class="my-container">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <h3 class="mb-3">Succesfully trained</h3>
                        <h2 class="highlight my-2">{{ firstcount }}</h2>
                        <p class="text-uppercase grey-text">Enrolled learners</p>
                    </div>
                    <div class="col">
                        <h3 class="mb-3">Proudly received</h3>
                        <h2 class="highlight my-2">{{ secondcount }}</h2>
                        <p class="text-uppercase grey-text">Countrywide Awards</p>
                    </div>
                    <div class="col">
                        <h3 class="mb-3">Firmly established</h3>
                        <h2 class="highlight my-2">{{ thirdcount }}</h2>
                        <p class="text-uppercase grey-text">Local Branches</p>
                    </div>
                    <div class="col">
                        <h3 class="mb-3">Getting featured on</h3>
                        <h2 class="highlight my-2">{{ fourthcount }}</h2>
                        <p class="text-uppercase grey-text">Blog Posts</p>
                    </div>
                </div>
            </div>
        </div>
    </article>
</template>

<script>
export default {
    data() {
        return {
            firstcount: 0,
            secondcount: 0,
            thirdcount: 0,
            fourthcount: 0,
            intervalId: null,

        }
    },
    mounted() {
        const options = {
            root: null, // Il root element, null per l'intera viewport
            rootMargin: '0px', // Margini aggiuntivi attorno al root element
            threshold: 0.5 // Soglia di visibilità dell'elemento (0.5 = almeno il 50% dell'elemento deve essere visibile)
        };

        const observer = new IntersectionObserver(this.handleIntersection, options);
        observer.observe(this.$refs.elementToWatch);
    },
    methods: {
        handleIntersection(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    // L'elemento è diventato visibile
                    this.first(); // Chiamata alla funzione che desideri eseguire
                    this.second();
                    this.third();
                    this.fourth();
                }
            });
        },
        first() {
            for (let i = 0; i <= 1790; i++) {
                setTimeout(() => {
                    this.firstcount = i;
                }, 100);
            }
        },
        second() {
            for (let i = 0; i <= 19; i++) {
                setTimeout(() => {
                    this.secondcount = i;
                }, 1000);
            }
        },
        third() {
            for (let i = 0; i <= 24; i++) {
                setTimeout(() => {
                    this.thirdcount = i;
                }, 1000);
            }
        },
        fourth() {
            for (let i = 0; i <= 1090; i++) {
                setTimeout(() => {
                    this.fourthcount = i;
                }, 200);
            }
        }


    }
}


</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

article.hero {
    background-color: $footerColor;

    .row,
    .container {
        background-color: white;
    }

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