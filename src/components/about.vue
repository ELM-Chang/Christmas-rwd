<template>
    <div class="main">
        <section class="about section" id="about">
            <div class="about__container container grid">
                <div class="about__data">
                    <h2 class="section__title">
                        About sharing <br>
                        Happiness
                    </h2>
                    <p class="about__description">
                        Lorem ipsum dolor sit amet consectetur ad, 
                        odio sunt tenetur voluptatibus possimus minus consequatur, 
                        facere inventore optio vero consequuntur architecto porro.
                    </p>
                    <a href="###" class="button">Share Now</a>
                </div>
                <img src="../assets/img/about-christmas.png" alt="" class="about__img">
                <img src="../assets/img/snow-img.png" alt="about image" class="about__snow-1">
                <img src="../assets/img/snow-img.png" alt="about image" class="about__snow-2">
            </div>
        </section>
    </div>
</template>
<script setup>

</script>
<style scoped>
    .about__container {
        position: relative;
        row-gap: 3.5rem;
    }
    .about__data {
        text-align: center;
    }
    .about__description {
        margin-bottom: 2rem;
    }
    .about__img {
        width: 320px;
        justify-self: center;
    }
    .about__snow-1,
    .about__snow-2 {
        width: 50px;
        position: absolute;
    }
    .about__snow-1 {
        top: 12rem;
        left:1.5rem;
        animation: var(--animate-snow-1);
    }
    .about__snow-2 {
        right: -0.75rem;
        bottom: 0.5rem;
        animation: var(--animate-snow-2);
    }
    .button {
        display: inline-block;
        background: var(--first-color);
        padding: 1rem 2rem;
        border-radius: 4rem;
        color: var(--white-color);
        font-weight: var(--font-medium);
        transition: background 0.4s, box-shadow 0.4s;
    }
    .button:hover {
        background: var(--forst-color-alt);
        box-shadow: 0 8px 32px hsla(210, 80%, 54%, 0.7);
    }
</style>


