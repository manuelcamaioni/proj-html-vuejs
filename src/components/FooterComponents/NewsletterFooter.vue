<template>
    <section class="hero">
        <div class="my-container d-flex flex-column justify-content-center align-items-center py-5 position-relative">

            <div class="container-float-images" @mousemove="moveElements">
                <div class="double-semi-circle" :style="{ top: element1.y + 'px', left: element1.x + 'px' }"> </div>
                <div div class="dot-square" :style="{ top: element2.y + 'px', left: element2.x + 'px' }"></div>
            </div>

            <h2>Subscribe <span class="highlight">Newsletter</span></h2>
            <p>Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
            <div class="input-element d-flex">
                <input type="text" placeholder="Enter your email">
                <button class="btn">Subscribe</button>
            </div>

        </div>
    </section>
</template>

<script>

export default {

    data() {
        return {
            element1: {
                x: 0,
                y: 0
            },
            element2: {
                x: 0,
                y: 0
            },
            offset1: {
                offsetX: 0,
                offsetY: 30
            },
            offset2: {
                offsetX: 700,
                offsetY: 0
            }
        }
    },
    methods: {
        moveElements(event) {
            const containerRect = event.currentTarget.getBoundingClientRect();

            const containerCenterX = containerRect.left + containerRect.width / 2;
            const containerCenterY = containerRect.top + containerRect.height / 2;

            const maxMovement = 10;
            const mouseX = event.clientX;
            const mouseY = event.clientY;

            const offsetX = (mouseX - containerCenterX) / containerRect.width;
            const offsetY = (mouseY - containerCenterY) / containerRect.height;

            this.element1.x = offsetX * maxMovement + this.offset1.offsetX;
            this.element1.y = offsetY * maxMovement + this.offset1.offsetY;

            this.element2.x = -offsetX * maxMovement + this.offset2.offsetX;
            this.element2.y = -offsetY * maxMovement + this.offset2.offsetY;
        }
    }
}
</script>

<style lang="scss" scoped>
@use "../../styles/variables.scss" as *;

section.hero {
    font-weight: bold;
    color: $primaryColor;

    .container-float-images {
        width: 100%;
        height: 100%;
        position: absolute;
    }

    .double-semi-circle {
        background: url("../../assets/img/maxcoach-shape-02.png");
    }

    .dot-square {
        background: url("../../assets/img/maxcoach-shape-09.png")
    }

    .double-semi-circle,
    .dot-square {
        position: absolute;
        transition: all 0.2s ease-out;
        width: 100px;
        height: 100px;
        background-size: contain;
        background-repeat: no-repeat;
        z-index: auto;
    }

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
    width: 80%;
}

button {
    background-color: $primaryHighlight;
    border-radius: 0;
    color: white;
    font-size: .7rem;
    width: 20%;
}
</style>