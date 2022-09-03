<script setup lang="ts">
    import { gsap } from 'gsap';

    const MainDrone = ref<HTMLDivElement>(null)
    const droneTooltip = ref<HTMLImageElement>(null)
    const mainDroneTitle = ref<HTMLElement>(null)
    const mainDroneAbout = ref<HTMLDivElement>(null)


        onMounted(() => {
            const tl = gsap.timeline()
            tl.from(MainDrone.value, {duration:1, opacity:0, ease:"power3.inOut",scale:2.5, }, "<0.1")
            tl.from(droneTooltip.value,{opacity:0, y:100, ease:"power3.inOut"}, "<0.2")
            tl.fromTo(mainDroneTitle.value,  {y: 0, opacity: 0, }, { opacity:1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"}, "<0.1");;
            tl.fromTo(mainDroneAbout.value.children[0], {y: 0, opacity: 0, }, { opacity:1, delay:.4, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"}, )
            tl.fromTo(mainDroneAbout.value.children[1],{y: 0, opacity: 0, }, { opacity:1, delay:.6, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)"}, )
        })

</script>

<template>
    <div class="hidden lg:flex absolute fixed w-full h-full ">

        <div class="flex flex-col ">
            <img src="~/assets/images/main.svg" class="w-8/12 bottom-32 object-fit absolute left-[25%]  "  ref="MainDrone" />

            <img src="~/assets/images/tooltip.svg" class="w-2/12 absolute bottom-56 left-[65%] " ref="droneTooltip" />

            <div class="absolute bottom-32 left-[82%] flex flex-col text-white">
                <h2 class="text-2xl font-[sans-light] font-semibold pl-4 " ref="mainDroneTitle">Mount Series 1</h2>
                <div class="flex gap-4">
                    <img src="~/assets/images/bar.svg"/>
               <div ref="mainDroneAbout">
                <li class="font-[open-sans]">Night Vision</li>
                <li class="font-[open-sans]">19 Hours Battery life</li>
               </div>
            </div>
            </div>
        </div>
    </div>
</template>