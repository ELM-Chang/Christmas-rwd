<template>
    <div>
        <navigation></navigation>
        <home></home>
        <about></about>
        <send></send>
        <foot_component></foot_component>
        <scroll_up></scroll_up>
    </div>
</template>
<script setup>
    import navigation from "../components/navigation.vue"
    import home from "../components/home.vue"
    import about from "../components/about.vue"
    import send from "../components/send.vue"
    import foot_component from "../components/foot_component.vue"
    import scroll_up from "../components/scroll_up.vue"
    import {onMounted} from 'vue'
    onMounted(()=>{
        const observer = new IntersectionObserver((entries)=>{
            const addNavClass = (target)=>{
                const selectedLink = document.querySelector('.nav__menu a[href*='+target+']')
                selectedLink.classList.add('active-link')
            }
            const removeNavClass = (target)=>{
                const selectedLink = document.querySelector('.nav__menu a[href*='+target+']')
                selectedLink.classList.remove('active-link')
            }
            entries.forEach(e=>{
                if (e.intersectionRatio>0){
                    addNavClass(e.target.classList[0])
                } 
                else {
                    removeNavClass(e.target.classList[0])
                }
            })
        })
        const section=document.querySelectorAll('section[id]')
        section.forEach(s=>{
            observer.observe(s)
        })
        gsap.from('.home__village', 1.2, {opacity: 0, y: 100, delay: 0.1})
        gsap.from('.home__pine', 1.2, {opacity: 0, y: 100, delay: 0.7})
        gsap.from('.home__mountain-1', 1.2, {opacity: 0, y: 250, delay: 0.6})
        gsap.from('.home__mountain-2', 1.2, {opacity: 0, x: 150, delay: 0.3})
        gsap.from('.home__mountain-3', 1.2, {opacity: 0, x: -150, delay: 0.5})
        gsap.from('.home__moon', 1.2, {opacity: 0, y: 200, delay: 0.8})
        gsap.from('.home__trineo', 1.2, {opacity: 0, x: -200, delay: 0.8})
        gsap.from('.home__title', 1.2, {opacity: 0, y: -60, delay: 1})
    })
</script>
<style>
    ::-webkit-scrollbar {
        width: .6rem;
        border-radius: .5rem;
        background: hsl(210, 8%, 15%);
    }
    ::-webkit-scrollbar-thumb {
        background: hsl(210, 8%, 25%);
        border-radius: .5rem;
    }
    ::-webkit-scrollbar-thumb:hover {
        background: hsl(210, 8%, 35%);
    }
</style>