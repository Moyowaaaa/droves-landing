<script setup lang="ts">
    import {gsap} from "gsap"

    const mainSection = ref<HTMLDivElement>(null)
    const heroSection = ref<HTMLDivElement>(null)
    const heroHeader = ref<HTMLDivElement>(null)
    const heroText = ref<HTMLDivElement>(null)
    const MainDrone = ref<HTMLDivElement>(null)
    const fadedText = ref<HTMLDivElement>(null)
    const heroButtons = ref<HTMLDivElement>(null)



        onMounted(() =>{
            const tl = gsap.timeline()
            tl.from(mainSection.value, {opacity:0,delay:0.1,duration:0.3,ease:"power3.inOut"})
             tl.fromTo(heroSection.value, {opacity: 0 }, { opacity: 1 });
              tl.to(heroHeader.value, { y: 0, opacity: 1, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" }, "<0.1");
            tl.from(fadedText.value, {opacity:0, duration:.8, y:"100", ease:"power3.inOut"})
            tl.from(heroText.value,{opacity:0, duration:.8, y:"-100", ease:"power3.inOut"}, "-=1")
            tl.from(heroButtons.value, {opacity:0, duration:.8, y:"-100", ease:"power3.inOut"}, "-=1")


            
        })

</script>







<template>
    <div class="main h-screen mb-[5rem] lg:mb-0" ref="mainSection">
        
        <div class=" w-full flex  h-full flex-col ">

            <Navbar />

            <div class="flex h-full h-full" ref="heroSection">
            <div class="w-full lg:w-8/12 h-full pl-4 lg:pl-20 flex flex-col gap-12 mt-[15vh] lg:mt-0 lg:justify-center">
              <h1 class="text-4xl lg:text-6xl font-extrabold font-[sans-extra] z-50 " ref="heroHeader">Fly With The Birds</h1>  
              
              
              <p class="font-normal font-[open-sans] text-2xl" ref="heroText">Go beyond the mountains and into the valleys</p>

              <div class="flex gap-4" ref="heroButtons">
                <button class="p-4 lg:p-6 flex items-center justify-center bg-[black] text-[white] text-sm lg:text-2xl font-semibold font-[sans-light]">
                   <p > Mount Series 1 </p>  
                </button>

                <button class="p-4 lg:p-6 flex items-center justify-center border-2 border-[black] text-sm lg:text-2xl font-semibold font-[sans-light]" >
                    <p>Valley Series 1</p>
                </button>
              </div>
            </div>

            <!-- <div class="hidden lg:flex absolute right-48 top-24 h-4/6 w-full object-cover" ref="MainDrone">
            <img src="~/assets/images/main.svg" class="h-full w-full object-cover">
            <div class="absolute top-4 left-96">
                <img src="~/assets/images/tooltip.svg" />
            </div>
        </div> -->

        <DroneBanner />


        </div>


        <div class="absolute fade pb-0 lg:pb-3" >
            <h2 class="text-6xl font-black text-black" ref="fadedText">Droves</h2>
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
	
    background:  linear-gradient(180deg, rgba(0, 0, 0, 0.16) 0%, rgba(0, 0, 0, 0) 80.31%);
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
    overflow: hidden;

    

}   

@media screen and (max-width:485px) {
    .main{
        background-image:none;
        background-size:cover
    }

    .fade h2 {
        font-size:90px;
    }
}

</style>