<template>
    <div class="brands-list">
        <div class="my-container">
            <ul class="d-flex m-0 p-0 justify-content-between">
                <li v-for="brand in brands" class="brands-container">
                    <img :src="getImagePath(brand.path)" :alt="brand.path">
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            brands: [
                {
                    path: "client-logo-01.png",
                },
                {
                    path: "client-logo-02.png",
                },
                {
                    path: "client-logo-03.png",
                },
                {
                    path: "client-logo-04.png",
                },
                {
                    path: "client-logo-05.png",
                },
                {
                    path: "client-logo-06.png",
                },
                {
                    path: "client-logo-07.png",
                },
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

.brands-container {
    width: calc(100% / 7 - 1rem);
    height: 50px;

    img {
        width: 100%;
        height: 100%;
        object-fit: contain;
        opacity: 0.5;
    }
}
</style>