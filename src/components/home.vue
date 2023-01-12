<template>
    <div class="main">
        <section class="home section" id="home">
            <h1 class="home__title">Marry Christmas</h1>
            <img src="../assets/img/home-moon.png" alt="home img" class="home__moon">
            <img src="../assets/img/home-trineo-santa.png" alt="trineo img" class="home__trineo">
            <img src="../assets/img/home-mountain-3.png" alt="" class="home__mountain-3">
            <img src="../assets/img/home-mountain-2.png" alt="" class="home__mountain-2">
            <img src="../assets/img/home-pine-tree.png" alt="" class="home__pine">
            <img src="../assets/img/home-village.png" alt="" class="home__village">
            <img src="../assets/img/home-snow.png" alt="" class="home__snow">
            <img src="../assets/img/home-mountain-1.png" alt="" class="home__mountain-1">
            <img src="" alt="" class="home__">
            <img src="" alt="" class="home__">
        </section>
    </div>
</template>
<script setup>

</script>
<style scoped>
    .home {
        position: relative;
        background: linear-gradient(180deg,
        hsl(210,88%,20%),
        hsl(210,70%,50%)
        );
        height: 658px;
        padding-top: 7rem;
        overflow: hidden;
    }
    .home__title {
        color: var(--white-color);
        font-size: var(--biggest-font-size);
        font-family: var(--second-font);
        text-align: center;
        margin-top: 1.5rem;
    }
    .home img {
        position: absolute;
    }
    .home__mountain-1,
    .home__snow  {
        bottom:0;
    }
    .home__village,
    .home__pine,
    .home__moon,
    .home__trineo {
        left: 0;
        right: 0;
        margin: 0 auto;
    }
    .home__village {
        width: 260px;
        bottom: 1rem;
    }
    .home__pine {
        width: 240px;
        bottom: 4rem;
    }
    .home__mountain-2 {
        bottom: 3rem;
    }
    .home__mountain-3 {
        bottom: 6rem;
    }
    .home__moon {
        width: 300px;
        bottom: 8.5rem;
    }
    .home__trineo {
        width: 250px;
        bottom: 14.5rem;
    }
</style>
<style src="../breakpoint.css" scoped></style>