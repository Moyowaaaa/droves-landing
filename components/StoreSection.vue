<script setup lang="ts">
   import {gsap} from "gsap"
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
      gsap.registerPlugin(ScrollTrigger)

      const storeSection = ref<HTMLDivElement>(null)
      const storeHeadText = ref<HTMLElement>(null)
      const imageGrid = ref<HTMLDivElement>(null)
        const mountSeries = ref<HTMLDivElement>(null)
        const valleySeries = ref<HTMLDivElement>(null)
        const drovesSeries= ref<HTMLDivElement>(null)


        onMounted(() => {
            let tl = gsap.timeline({
                scrollTrigger: {
                    trigger:storeSection.value,
                    start: "top center",
                    
                  
                }
            })
            tl.to(storeHeadText.value, { y: 0, opacity: 1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" }, "<0.1");
            tl.from(imageGrid.value, {opacity:0, duration:.8, y:"100", ease:"power3.inOut"})
            tl.fromTo(mountSeries.value, {y: 0, opacity: 0, }, { opacity:1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"});;
            tl.fromTo(valleySeries.value, {y: 0, opacity: 0, }, { opacity:1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"}, "<0.3");;
            tl.fromTo(drovesSeries.value, {y: 0, opacity: 0, }, { opacity:1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"}, "<0.5");;
        })
    


</script>



<template>
    <div class="h-screen w-full flex flex-col mt-[6rem] lg:mt-0" ref="storeSection">
        <h2 class="text-[gotham-bold] text-center text-4xl mb-[2rem]" ref="storeHeadText">DROVES</h2>

        <div class="grid " ref="imageGrid">
            <div class="w-auto shadow-2xl ">
                <img src="~/assets/images/drone5.svg" class="cover-image">
                <div class="py-8 pl-4" ref="mountSeries">
                <p class="text-3xl font-bold font-[gotham-bold]">Mount Series 1</p>
                <p class="font-[gotham-light]">$299.99</p>
                </div>
            </div>
            

            <div class="w-auto shadow-2xl">
                <img src="~/assets/images/drone6.svg" class="cover-image">
                <div class="py-8 pl-4" ref="valleySeries">
                <p class="text-3xl font-bold font-[gotham-bold]" > Valley Series 1</p>
                <p class="font-[gotham-light]">$249.99</p>
                </div>  
</div>

<div class="w-auto shadow-2xl">
    <img src="~/assets/images/drone7.svg" class="cover-image">
    <div class="py-8 pl-4" ref="drovesSeries">
    <p class="text-3xl font-bold font-[gotham-bold]" >Droves Series 1</p>
    <p class="font-[gotham-light]">$199.99</p>
    </div>
</div>
        </div>

        <ShopBanner />
        <Footer />
    </div>
</template>


<style scoped>
 .grid {
        grid-template-columns: repeat(auto-fit, minmax(22.2rem, 1fr));
        gap: 3rem;
        padding-left:5%;
        padding-right:5%;
    }

    .cover-image {
        width: 100%;
        margin: 0 auto;
        max-width: 100%;
        object-fit: cover;
        
    }


    @media screen and (max-width:485px) {
        .grid{
            padding-right:0;
            padding-left:0;
            grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
        }
        
    }

</style>