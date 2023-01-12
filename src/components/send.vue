<template>
    <div class="main">
        <section class="send section" id="send">
            <h2 class="section__title">
                Send love This <br>
                Christmas
            </h2>
            <div class="send__container container grid">
                <div class="send__card">
                    <img src="../assets/img/send-night.png" alt="send img" class="send__img">
                    <h3 class="send__title">Spend It With Family</h3>
                    <p class="send__description">
                        Sharing with family is best gift you can give.
                    </p>
                </div>
                <div class="send__card">
                    <img src="../assets/img/send-gifts.png" alt="send img" class="send__img">
                    <h3 class="send__title">Give Lots Of Love</h3>
                    <p class="send__description">
                        send a gift and lot of love
                        to those most in need. 
                    </p>
                </div>
                <div class="send__card">
                    <img src="../assets/img/send-santa.png" alt="send img" class="send__img">
                    <h3 class="send__title">Share Good Wishes</h3>
                    <p class="send__description">
                        Wish good messages to loved
                        one this christmas.
                    </p>
                </div>
                <img src="../assets/img/snow-img.png" alt="" class="send__snow-1">
                <img src="../assets/img/snow-img.png" alt="" class="send__snow-2">
                <img src="../assets/img/snow-img.png" alt="" class="send__snow-3">
            </div>
        </section>
        <section class="celebrate section" id="celebrate">
            <div class="celebrate__container container grid">
                <div class="celebrate__data">
                    <h2 class="section__title">
                        Celebrate With A <br>
                        Lot Of Love
                    </h2>
                    <p class="celebrate__description">
                        In this holiday, celebrate with much love and peace,
                        offering many blessing to our loved ones, 
                        friends and neighbors, wishing them a good Christmas message.
                    </p>
                    <a href="###" class="button">Celebrate Now!</a>
                </div>
                <img src="../assets/img/celebarte-church.png" alt="celebrate image" class="celebrate__img">
                <img src="../assets/img/snow-img.png" alt="celebrate image" class="celebrate__snow-1">
                <img src="../assets/img/snow-img.png" alt="celebrate image" class="celebrate__snow-2">
            </div>
        </section>
    </div>
</template>
<script setup>

</script>
<style scoped>
    .send__container {
        position:relative;
        grid-template-columns: 200px;
        justify-content: center;
        row-gap: 3rem;
        padding-top: 1.5rem;
    }
    .send__card {
        text-align: center;
    }
    .send__img {
        width: 180px;
        margin-bottom: .75rem;
    }
    .send__title {
        font-size: var(--h3-font-size);
        margin-bottom: .5rem;
    }
    .send__description {
        font-size: var(--small-font-size);
        padding-inline: 1.5rem;
    }
    .send__snow-1,
    .send__snow-2,
    .send__snow-3 {
        width: 50px;
        position: absolute;
    }
    .send__snow-1 {
        left:0;
        top:7rem;
        animation: var(--animate-snow-1);
    }
    .send__snow-2 {
        top:23rem;
        right:0;
        animation: var(--animate-snow-2);
    }
    .send__snow-3 {
        bottom:9rem;
        left:0;
        animation: var(--animate-snow-1);
    }
    /* ===============celebrate================== */
    .celebrate__container {
        position: relative;
        row-gap: 3.5rem;
    }
    .celebrate__data {
        text-align: center;
    }
    .celebrate__description {
        margin-bottom: 2rem;
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
    .celebrate__img {
        width: 320px;
        justify-self: center;
    }
    .celebrate__snow-1,
    .celebrate__snow-2 {
        width: 50px;
        position: absolute;
    }
    .celebrate__snow-1 {
        top:1.5rem;
        left:1.5rem;
        animation: var(--animate-snow-1);
    }
    .celebrate__snow-2 {
        top:18rem;
        right:0;
        animation: var(--animate-snow-2);
    }
</style>
<style src="../breakpoint.css" scoped></style>