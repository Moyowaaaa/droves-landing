<script setup lang="ts">
    import {gsap} from 'gsap'

    const navbar = ref<HTMLElement>(null)
    const navLogo = ref<HTMLDivElement>(null)
    const navLinks = ref<HTMLDivElement>(null)

        onMounted(() => {
            const tl = gsap.timeline()
            tl.from(navbar.value, {opacity:0})
            tl.from(navLogo.value, { y: -50, opacity: 0 })
           tl.from(navLinks.value.children, { x: 20, opacity: 0, stagger: 0.2 }, "-=0.5");
        })

</script>


<template>
    <div>
        <div class="w-full h-[4rem]   flex items-center  justify-between px-20" ref="navbar">
            <div ref="navLogo">
                <h2 class="font-[gotham-bold] text-3xl">Droves</h2>
            </div>
            
            <div class="flex items-center gap-4 text-white font-[gotham-light]" ref="navLinks">
                <p>About</p>
                <p>Support</p>
                <p>Explore</p>
                <button class="px-6 py-2  font-[gotham-bold] bg-[white] text-black">Shop</button>
            </div>
        </div>
    </div>
</template>

