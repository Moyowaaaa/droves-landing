<script setup lang="ts">
    import {gsap} from "gsap"
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
      gsap.registerPlugin(ScrollTrigger)



    const aboutSection = ref<HTMLDivElement>(null)
    const aboutSectionText = ref<HTMLElement>(null)
    const aboutTextMainImage = ref<HTMLImageElement>(null)
    const aboutSectionHead = ref<HTMLElement>(null)
    const aboutImage1 = ref<HTMLImageElement>(null)
    const aboutImage2 = ref<HTMLImageElement>(null)
    const aboutImage3 = ref<HTMLImageElement>(null)
    const seeMore = ref<HTMLElement>(null)

        onMounted(() => {
           
    

let tl = gsap.timeline({scrollTrigger: {
    trigger:aboutSection.value,
    start:"top center",
   
}})

tl.to(aboutSectionHead.value, { y: 0, opacity: 1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" }, "<0.1");
 tl.from(aboutSectionText.value, {  opacity: 0, y:"-100%",  ease:"power3.easeinOut",}, "<0.1");
 tl.from([aboutImage1.value, aboutImage2.value, aboutImage3.value] , {  opacity: 0, y:"-100%", duration:.9, stagger:.6,  ease:"power3.easeinOut",}, "<0.1")
  tl.from(aboutTextMainImage.value, {duration:1, opacity:0, ease:"power3.inOut",scale:2.5, }, "<0.1")
  tl.from(seeMore.value, {  opacity: 0, y:"-100%",  ease:"power3.easeinOut",}, "<0.1");

        })
 

</script>



<template>
    <div class="about h-auto w-full flex flex-col mt-[5rem] "  ref="aboutSection">


        <div class="h-max lg:h-[600px] lg:px-[5%] ">
            <div class="w-full h-full flex flex-col gap-4 items-center lg:items-end lg:flex-row">

                
                <div class="h-full w-11/12 lg:w-5/12 ">
                    <img src="~/assets/images/drone1.svg " class="object-cover w-full h-full " ref="aboutTextMainImage">
                </div>


                <div class=" w-11/12 lg:w-7/12 flex flex-col gap-6 lg:gap-4 ">

                 
                    <h2 class="font-[gotham-bold] font-bold text-3xl" ref="aboutSectionHead">Fly It Anywhere</h2>
                <p class="lg:w-10/12  text-xl lg:text-2xl font-[gotham-light] font-[400]" ref="aboutSectionText">With advanced technology in place to reach great heights and
depths Droves gives to the opportunity with our various range
of drones to reach those limits.</p>

                <div class="bordr-2 border-[teal] w-full flex justify-end font-[gotham-bold]" ref="seeMore">
                    See More
                </div>

                    <div class="w-full flex flex-col lg:flex-row gap-2  lg:space-x-4">
                        <img src="~/assets/images/drone2.svg"  loading="lazy" class="object-cover w-full" ref="aboutImage1"/>

                        <img src="~/assets/images/drone3.svg" loading="lazy" class="object-cover w-full" ref="aboutImage2"/>

                        <img src="~/assets/images/drone4.svg" loading="lazy" class="object-cover w-full" ref="aboutImage3"/>
                    </div>
                </div>

              


            





            </div>
        </div>

        <FeaturesBanner /> 


            

        
        
       




       
    </div>
</template>



<style scoped>

/* .grid {
        grid-template-columns: repeat(auto-fit, minmax(22.2rem, 4fr));
      
        padding-left:5%;
        padding-right:5%;
    } */



.drone1{
    background: url('../assets/images/drone1.svg');
    background-size: cover;
    background-repeat: no-repeat;
}

</style>
