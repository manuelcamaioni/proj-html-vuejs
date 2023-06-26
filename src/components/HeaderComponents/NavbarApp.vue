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



    .logoApp {
        width: 140px;



        img {
            width: 100%;

            object-fit: cover;
        }
    }
}
</style>