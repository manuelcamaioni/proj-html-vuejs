<template>
    <nav>
        <div class="my-container h-100 d-flex align-items-center justify-content-between">
            <div class="logoApp">
                <img src="../../assets/img/dark-logo.png" alt="">
            </div>
            <div class="nav-links">
                <ul class="d-flex">
                    <li>link</li>
                    <li>link</li>
                    <li>link</li>
                </ul>
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
    border: 1px solid black;
    height: 60px;

    .logoApp {
        border: 1px solid violet;
        height: 30px;


        img {
            height: 100%;
            width: 100%;
        }
    }
}
</style>