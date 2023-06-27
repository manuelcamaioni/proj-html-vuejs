<template>
    <nav>
        <div class="my-container h-100 d-flex align-items-center">
            <div class="logoApp">
                <img src="../../assets/img/dark-logo.png" alt="">
            </div>

        </div>
    </nav>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

nav {

    box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 25px -5px, rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;
    height: 60px;

    .logoApp {
        width: 140px;



        img {
            width: 100%;

            object-fit: cover;
        }
    }
}
</style>