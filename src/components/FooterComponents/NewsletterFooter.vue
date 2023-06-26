<template>
    <section class="hero">
        <div class="my-container">
            <h1>Subscribe <span>Newsletter</span></h1>
            <p>Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
            <div class="input-element d-flex">
                <input type="email" placeholder="Enter your email">
                <button class="btn">Subscribe</button>
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.input-element {
    border-radius: 0.375rem;
    overflow: hidden;
    background-color: black;
    width: fit-content;
}

input {
    border: none;
    border-radius: 0;
}

button {
    background-color: red;
    border-radius: 0;

}
</style>