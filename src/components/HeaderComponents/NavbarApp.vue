<template>
    <nav>
        <div class="my-container h-100 d-flex align-items-center">
            <div class="logoApp h-100 d-flex align-items-center px-5 w-25">
                <img src="../../assets/img/dark-logo.png" alt="">
            </div>
            <div class="my-dropdown-menu h-100 px-2 w-50">
                <ul class="d-flex h-100">
                    <li v-for="(element, index) in navData"
                        class="link-element h-100 position-relative d-flex align-items-center justify-content-center">{{
                            element.link
                        }} <span class="toggle-sub-menu ms-1">&#9660;</span>
                        <div class="my-single-dropdown position-absolute d-flex"
                            :class="navData[index].content.length > 15 ? 'custom' : ''">
                            <ul class="d-flex flex-column flex-wrap h-100">
                                <li v-for="string in navData[index].content" class="link-dropdown"><a href="#">{{ string
                                }}</a></li>

                            </ul>
                            <div v-if="navData[index].content.length > 15"
                                class="img-container h-100 d-flex align-items-center pe-2">
                                <img src="../../assets/img/homepages-mega-menu-image-alt.jpg" alt="">
                            </div>
                        </div>

                    </li>
                </ul>
            </div>
            <div class="my-search-container h-100 d-flex align-items-center w-25">

                <div class="my-searchbar d-flex align-items-center justify-content-evenly position-relative">
                    <div class="user-icon-container"><i class="fa-regular fa-user fa-sm"></i></div>
                    <input type="text" class="w-75" placeholder="Search">
                    <i class="fa-solid fa-magnifying-glass position-absolute"></i>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    props: {
        navData: Array
    },

}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;



nav {

    box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 25px -5px, rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;
    height: 60px;
    background-color: white;
    width: 100vw;
    position: fixed;
    z-index: 2;

    .logoApp {
        width: 140px;

        img {
            width: 100%;
            object-fit: cover;
        }
    }

    .my-dropdown-menu li.link-element {
        font-size: .65rem;
        padding: .5rem;
        width: calc(100% / 6);
        cursor: pointer;
        transition: color .5s;

        span.toggle-sub-menu {
            font-size: .4rem;
        }
    }

    .my-dropdown-menu li.link-element:hover {
        color: $primaryHighlight;
    }


    .my-dropdown-menu li.link-element::after {
        content: '';
        position: absolute;
        top: 99%;
        right: 100%;
        bottom: 0;
        left: 0;
        background-color: $primaryHighlight;
        transition: all .5s;
    }

    .my-dropdown-menu li.link-element:hover::after {
        right: 0;
    }

    .my-single-dropdown {
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
        top: 120%;
        opacity: 0;
        pointer-events: none;
        width: 150px;
        background-color: white;
        transition: all .5s ease-out;

        ul {
            width: 100%;
            padding: 0.3rem;
        }

        li.link-dropdown {
            font-size: .7rem;
            padding: 0.5rem;
            width: fit-content;

            a {
                text-decoration: none;
                color: grey;
                transition: color .5s;
            }

            a:hover {
                color: $primaryHighlight;
            }
        }

        .img-container {
            width: 55%;

            img {
                width: 100%;
            }
        }
    }

    div.my-single-dropdown.custom {
        width: 600px;
        height: 400px;
    }

    .my-single-dropdown.custom ul {
        width: 45%;
    }

    .my-dropdown-menu li.link-element:hover .my-single-dropdown {
        opacity: 1;
        pointer-events: auto;
        top: 90%;
    }

    .user-icon-container i {
        transition: color .5s;
        font-size: .7rem;
    }

    .user-icon-container:hover i {
        color: $primaryHighlight;
    }

    .my-searchbar input {
        outline: none;
        border: none;
        background-color: #f8f8f8;
        border-radius: 0.375rem;
        padding: .2rem .6rem .2rem .3rem;
        font-size: .6rem;
    }

    .my-searchbar input:focus {
        border: 1px solid $primaryHighlight;
    }

    input::placeholder {
        font-size: .7rem;
    }

    .my-searchbar i {
        right: 15px;
        font-size: .7rem;
    }
}
</style>