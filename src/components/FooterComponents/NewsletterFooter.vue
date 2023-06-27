<template>
    <section class="hero">
        <div class="my-container d-flex flex-column justify-content-center align-items-center py-5">
            <h2>Subscribe <span class="highlight">Newsletter</span></h2>
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
@use "../../styles/variables.scss" as *;

section.hero {
    font-weight: bold;
    color: $primaryColor;

    h2 {
        text-align: center;
        font-size: 1.5rem;
    }

    p {
        color: $secondaryTextColor;
        text-align: center;
        font-size: .7rem;
    }
}

.input-element {
    border-radius: 0.375rem;
    overflow: hidden;
    background-color: black;
    font-size: .7rem;
    width: 50%;

}

input {
    border: none;
    border-radius: 0;
    width: 70%;
}

button {
    background-color: $primaryHighlight;
    border-radius: 0;
    color: white;
    font-size: .7rem;
    width: 30%;
}
</style>