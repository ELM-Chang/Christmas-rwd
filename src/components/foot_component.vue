<template>
    <div>
        <footer class="footer">
            <div class="footer__container container">
                <a href="###" class="footer__logo">Christmas</a>
                <ul class="footer__social">
                    <li>
                        <a href="" target="_blank" class="footer__social-link">
                            <i class="ri-facebook-fill"></i>
                        </a>
                    </li>
                    <li>
                        <a href="" target="_blank" class="footer__social-link">
                            <i class="ri-instagram-fill"></i>
                        </a>
                    </li>
                    <li>
                        <a href="" target="_blank" class="footer__social-link">
                            <i class="ri-twitter-fill"></i>
                        </a>
                    </li>
                </ul>
                <span class="footer__copy">
                    &#169;  Copyright Bedimcode. All right reserved.
                    Remake by Chang.
                </span>
                <img src="../assets/img/snow-img.png" alt="footer image" class="footer__snow-1">
                <img src="../assets/img/snow-img.png" alt="footer image" class="footer__snow-2">
            </div>
        </footer>
    </div>
</template>
<script setup>

</script>
<style scoped>
    .footer {
        overflow: hidden;
    }
    .footer__container {
        position: relative;
        padding-block: 4.5rem 2rem;
        text-align: center;
        height: 200px;
        z-index: var(--z-fixed);
    }
    .footer__logo,
    .footer__social-link,
    .footer__copy {
        color: var(--white-color);
    }
    .footer__logo {
        display: inline-block;
        font-size: var(--h2-font-size);
        font-family: var(--second-font);
        margin-bottom: 1rem;
    }
    .footer__social {
        display: flex;
        justify-content: center;
        column-gap: 1.5rem;
    }
    .footer__social-link {
        font-size: 1.25rem;
        transition: color .3s;
    }
    .footer__social-link:hover {
        color: var(--first-color);
    }
    .footer__copy {
        display: block;
        margin-top: 2rem;
        font-size: var(--smaller-font-size);
    }
    .footer__snow-1,
    .footer__snow-2 {
        position: absolute;
    }
    .footer__snow-1 {
        width:50px;
        top:4.5rem;
        left:0;
        animation: var(--animate-snow-1);
    }
    .footer__snow-2 {
        width: 70px;
        top:6.5rem;
        right:-3rem;
        animation: var(--animate-snow-2);
    }
</style>
<style src="../breakpoint.css" scoped></style>