<script setup lang="ts">
     import {gsap} from "gsap"
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
      gsap.registerPlugin(ScrollTrigger)


      const shopBanner = ref<HTMLDivElement>(null)
        const shopBannerContent = ref<HTMLDivElement>(null)


        onMounted(() => {
            let tl = gsap.timeline({
                scrollTrigger: {
                    trigger: shopBanner.value,
                    start: "top center",
                   
                    
                }
            })
            tl.fromTo(shopBannerContent.value.children[0], {y: 0, opacity: 0, }, { opacity:1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"});;
            tl.fromTo(shopBannerContent.value.children[1], {y: 0, opacity: 0, }, { opacity:1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"});;
          
        })

</script>


<template>
    <div class="shopbanner" ref="shopBanner">
    
       <div class="w-full py-[5rem] flex flex-col justify-center items-center">
        <div class="lg:flex flex-col gap-4 pl-2 lg:pl-[30rem]" ref="shopBannerContent">
        <h2 class="text-white text-xl lg:text-7xl font-bold font-[gotham-bold]">DROVES SERIES 1</h2>
        <button class="flex items-center justify-center text-black bg-white text-5xl font-bold font-[gotham-bold] w-max p-4">
            BUY NOW
        </button>
        </div>
       </div>
    </div>
</template>


<style scoped>

</style>