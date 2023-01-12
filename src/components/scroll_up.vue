<template>
    <div>
        <a href="#" class="scrollup" id="scroll-up">
            <i class="ri-arrow-up-line"></i>
        </a>
    </div>
</template>
<script setup>
const scrollUp = ()=>{
    const scrollArrow=document.getElementById('scroll-up')
    window.scrollY >=350    ?scrollArrow.classList.add('show-arrow')
                            :scrollArrow.classList.remove('show-arrow')
}
window.addEventListener('scroll', scrollUp)
</script>
<style scoped>
    .scrollup {
        position: fixed;
        right: 1rem;
        bottom: -50%;
        background: var(--white-color);
        display: inline-flex;
        padding: .45rem;
        border-radius: .45rem;
        font-size: 1rem;
        color: var(--body-color);
        z-index: var(--z-fixed);
        transition: bottom .3s, transform .3s;
    }
    .scrollup:hover {
        transform: translateY(-0.25rem);
    }
    .show-arrow {
        bottom: 3rem;
    }
</style>
<style src="../breakpoint.css" scoped></style>