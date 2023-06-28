<template>
    <section class="hero">
        <div class="my-container">
            <div class="footer-info d-flex">
                <div class="address-container">
                    <h4>Address</h4>
                    <ul>
                        <li>{{ addressData.address }}</li>
                        <li>{{ addressData.phone }}</li>
                        <li>{{ addressData.email }}</li>
                    </ul>
                </div>
                <div class="explore-container">
                    <h4>Explore</h4>
                    <div class="d-flex">
                        <ul class="me-2">
                            <li><a href="#">Start here</a></li>
                            <li><a href="#">Blog</a></li>
                            <li><a href="#">About us</a></li>
                        </ul>
                        <ul>
                            <li><a href="#">Success story</a></li>
                            <li><a href="#">Courses</a></li>
                            <li><a href="#">Contact us</a></li>
                        </ul>
                    </div>
                </div>
                <div class="info-container">
                    <h4>Information</h4>
                    <ul>
                        <li><a href="#">Membership</a></li>
                        <li><a href="#">Purchase guide</a></li>
                        <li><a href="#">Privacy policy</a></li>
                        <li><a href="#">Terms of service</a></li>
                    </ul>
                </div>
            </div>
            <div class="social-media">
                <i class="fa-brands fa-square-facebook"></i><i class="fa-brands fa-square-twitter"></i><i
                    class="fa-brands fa-instagram"></i><i class="fa-brands fa-linkedin"></i>
            </div>
            <div class="copyright">
                <span>&#169; 2020 MaxCoach, All Rights Reserved</span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    props: {
        addressData: Object
    }
}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

.footer-info {
    padding-top: 2rem;
}

.explore-container,
.info-container {
    width: 25%;

}

.address-container {
    width: 50%;
}

h4 {
    font-size: 0.8rem;
}

li {
    font-size: .7rem;

    a {
        color: $secondaryTextColor;
        text-decoration: none;
    }
}

.social-media i {
    color: #b1b1b1;
    margin: 0 .5rem;
}

.copyright {
    text-align: center;
    padding: 1rem 0;

    span {
        font-size: .6rem;
        color: #b1b1b1;


    }
}

i.fa-brands {
    transition: color .5s;

}

i.fa-brands:hover {
    color: $primaryHighlight;
}
</style>