<template>
    <div id="navComp">
        <header class="header" id="header">
            <nav class="nav container">
                <a href="###" class="nav__logo">
                    <img src="../assets/img/logo.png" alt="">
                    Christmas
                </a>
                <div class="nav__menu" id="nav--menu">
                    <ul class="nav__list">
                        <li class="nav__item">
                            <a href="#home" class="nav__link active-link">Home</a>
                        </li>
                        <li class="nav__item">
                            <a href="#about" class="nav__link">About</a>
                        </li>
                        <li class="nav__item">
                            <a href="#send" class="nav__link">Send</a>
                        </li>
                        <li class="nav__item">
                            <a href="#celebrate" class="nav__link">Celebrate</a>
                        </li>
                    </ul>
                    <!-- remix icon -->
                    <div class="nav__close" id="nav--close">
                        <i class="ri-close-line"></i>
                    </div>
                    <img src="../assets/img/snow-img.png" alt="" class="nav__img-1">
                    <img src="../assets/img/snow-img.png"  alt="" class="nav__img-2">
                </div>
                <div class="nav__toggle" id="nav--toggle">
                    <i class="ri-apps-2-line"></i>
                </div>
            </nav>
        </header>
    </div>
</template>
<script setup>
    import {onMounted} from 'vue'
    // decoupled with html, do not need @click
    onMounted(()=>{
        const navMenu=document.getElementById("nav--menu")
        const navToggle=document.getElementById("nav--toggle")
        const navClose=document.getElementById("nav--close")
        const navLink=document.querySelectorAll(".nav__link")
        const linkAction=()=>{
            navMenu.classList.remove('show-menu')
        }
        if(navToggle){
            navToggle.addEventListener('click', ()=>{
                navMenu.classList.add('show-menu')
            })
        }
        if(navClose){
            navClose.addEventListener('click', ()=>{
                navMenu.classList.remove('show-menu')
            })
        }
        navLink.forEach(e=> e.addEventListener('click', linkAction))
    })
    const scrollHeader=()=>{
        const header = document.getElementById('header')
        window.scrollY >= 50    ? header.classList.add('bg-header')
                                :header.classList.remove('bg-header')
    }
    window.addEventListener('scroll', scrollHeader)

</script>
<style scoped>
    header {
        background: transparent;
        position: fixed;
        top:0;
        left:0;
        width: 100%;
        transition: background 0.4s;
        z-index: var(--z-fixed);
    }
    nav {
        position: relative;
        height: var(--header-height);
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .nav__logo,
    .nav__toggle,
    .nac__close {
        display: flex;
        color:var(--white-color)
    }
    .nav__logo img {
        width: 30px;
        transform: rotate(-10deg);
    }
    .nav__logo {
        align-items: center;
        column-gap: .25rem;
        font-family: var(--second-font);
        font-size: var(--h2-font-size);
    }
    .nav__toggle {
        font-size: 1.5rem;
        cursor: pointer;
    }
    @media screen and (max-width:767px) {
        .nav__menu {
            position:fixed;
            top: -100%;
            left: 0;
            background: var(--body-color);
            width: 100%;
            padding-block: 3.5rem;
            transition: top 0.4s;
        }
    }
    .show-menu {
        top:0;
    }
    .bg-header {
        background: var(--body-color);
    }
    .nav__list {
        display: flex;
        flex-direction: column;
        text-align: center;
        row-gap: 2rem;
        cursor: pointer;
    }
    .nav__link {
        color: var(--white-color);
        font-weight: var(--font-medium);
        transition: color 0.4s;
    }
    .nav__link:hover {
        color: var(--first-color);   
    }
    .nav__close {
        position: absolute;
        top: 1rem;
        right: 1.5rem;
        font-size: 1.5rem;
        cursor: pointer;
    }
    .nav__img-1,
    .nav__img-2 {
        position: absolute;
    }
    .nav__img-1 {
        width: 40px;
        top: 6rem;
        left: 2.5rem;
        transform: rotate(-15deg);
    }
    .nav__img-2 {
        width: 60px;
        right: 1rem;
        bottom: 2rem;
        transform: rotate(15deg);
    }
    .active-link {
        color: var(--first-color);
    }
</style>
<style src="../breakpoint.css" scoped></style>