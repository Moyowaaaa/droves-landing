<script setup lang="ts">
    import {gsap} from "gsap"


    const heroSection = ref<HTMLDivElement>(null)
    const heroHeader = ref<HTMLDivElement>(null)
    const heroText = ref<HTMLDivElement>(null)
    const MainDrone = ref<HTMLDivElement>(null)
    const fadedText = ref<HTMLDivElement>(null)
    const heroButtons = ref<HTMLDivElement>(null)


        onMounted(() =>{
            const tl = gsap.timeline()
            tl.fromTo(heroSection.value, { opacity: 0 }, { opacity: 1 });
            tl.to(heroHeader.value, { y: 0, opacity: 1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" }, "<0.1");
            tl.to(heroButtons.value.children, { y: 0, opacity: 1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" }, "<0.1");
            tl.from(heroText.value, {  opacity: 0, y:"-100%",  ease:"power3.easeinOut",}, "<0.1");
            tl.from(MainDrone.value, {duration:1, opacity:0, ease:"power3.inOut",scale:2.5, }, "<0.1")
            tl.from(fadedText.value, { opacity:0, y:100, ease:"power2.inOut"}, ".8")
        })

</script>







<template>
    <div class="main h-screen">
        
        <div class=" w-full flex  h-full flex-col ">

            <Navbar />

            <div class="flex h-full h-full" ref="heroSection">
            <div class="w-8/12 h-full pl-20 flex flex-col gap-6 justify-center">
              <h1 class="text-7xl font-bold " ref="heroHeader">Fly With The Birds</h1>  
              
              
              <p class="font-normal text-2xl" ref="heroText">Go beyond the mountains and into the valleys</p>

              <div class="flex gap-4" ref="heroButtons">
                <button class="p-6 flex items-center justify-center bg-[black] text-[white] text-2xl">
                    Mount Series 1
                </button>

                <button class="p-6 flex items-center justify-center border-2 border-[black] text-2xl">
                    Valley Series 1
                </button>
              </div>
            </div>

            <div class="absolute right-48 top-24 h-4/6 w-[60vw] object-cover" ref="MainDrone">
            <img src="~/assets/images/main.svg" class="h-full w-full object-cover">
        </div>
        </div>


        <div class="absolute fade pb-3" ref="fadedText">
            <h2 class="text-6xl font-black text-black">Droves</h2>
        </div>
        </div>

        </div>  

</template>


<style scoped>

/* .fade{
   background:  linear-gradient(180deg, rgba(0, 0, 0, 0.16) 0%, rgba(0, 0, 0, 0) 70.31%);
    background-clip: text;
} */

.fade h2 {
	
    background:  linear-gradient(180deg, rgba(0, 0, 0, 0.16) 0%, rgba(0, 0, 0, 0) 70.31%);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
    font-size:150px;
}
.main{
    /* background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-position-x: 125vh;
  width:100%;
  height:100vh;
  background-color: #f2eee6;
  background-attachment: fixed;
    background: linear-gradient(to bottom, transparent,url('@/assets/images/mainbackground.png')) ; */
    
    width:100%;
    height: 100vh;
    background-image:url('@/assets/images/mainbackground.png'),
    linear-gradient(to right,transparent,transparent);
    background-repeat: no-repeat;
    background-position: right, left;
    background-size: 40%, 60%;

    

}   

</style>