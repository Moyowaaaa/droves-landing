<script setup lang="ts">
 import {gsap} from "gsap"
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
      gsap.registerPlugin(ScrollTrigger)

      const featuresBanner = ref<HTMLDivElement>(null)
      const drone4kText = ref<HTMLDivElement>(null)
      const droneFeatures = ref<HTMLDivElement>(null)

        onMounted(() => {
        
            let tl = gsap.timeline({
                scrollTrigger: {
                    trigger: featuresBanner.value,
                    start: "top=500 center",
                    scrub:true
                 
                    
                }
            })
            tl.from(drone4kText.value, {duration:1, opacity:0, ease:"power3.inOut",scale:2.5, }, "-=1")
            tl.from(droneFeatures.value.children[0], {  opacity: 0, y:"-100%",  delay:0.2,  ease:"power3.easeinOut",}, "-=1");
            tl.from(droneFeatures.value.children[1], {  opacity: 0, y:"-100%",  delay:0.4,  ease:"power3.easeinOut",}, "-=1");
            tl.from(droneFeatures.value.children[2], {  opacity: 0, y:"-100%",  delay:0.4,  ease:"power3.easeinOut",}, "-=1");
        })



</script>

<template>
    <div class="featuresbanner  overflow-x-hidden" ref="featuresBanner">
        <div class="w-full h-full flex flex-col lg:flex-row">

            <!-- <h1 class=" font-bold font-[gotham-bold] text-white">4K</h1> -->

            <div class="flex flex-col lg:flex-row justify-between w-full h-full items-center " ref="drone4kText">
                <img src="~/assets/images/4ktext.svg"/>

                <div class="flex flex-col gap-6 lg:pr-32 my-[3rem] lg:my-0" ref="droneFeatures">
                <div class="flex ">
                    <img src="~/assets/images/outline1.svg" class="hidden lg:flex"/>
                    <p class="font-[gotham-light] text-white">Still Image Resolution 60fps</p>
                </div>

                <div class="flex">
                    <img src="~/assets/images/outline2.svg" class="hidden lg:flex"/>
                    <p class="font-[gotham-light] text-white">Video resolution 4k</p>
                </div>


                <div class="flex">
                    <img src="~/assets/images/outline3.svg" class="hidden lg:flex"/>
                    <p class="font-[gotham-light] text-white">Recording at 100Mbps bitrate</p>
                </div>



            </div>

            </div>
           
        </div>
    </div>
</template>



<style scoped>

    
    </style>