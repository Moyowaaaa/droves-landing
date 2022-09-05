<script setup lang="ts">
    import {gsap} from "gsap"


    const aboutSection = ref<HTMLDivElement>()

        onMounted(() => {
           console.log(aboutSection.value)
         
        })
 

</script>



<template>
    <div class="about h-auto w-full flex flex-col mt-[5rem] "  ref="aboutSection">


        <div class="h-max lg:h-[600px] lg:px-[5%] ">
            <div class="w-full h-full flex flex-col gap-4 items-center lg:items-end lg:flex-row">

                
                <div class="h-full w-11/12 lg:w-5/12 ">
                    <img src="~/assets/images/drone1.svg " class="object-cover w-full h-full ">
                </div>


                <div class=" w-11/12 lg:w-7/12 flex flex-col gap-6 lg:gap-4 ">

                 
                    <h2 class="font-[gotham-bold] font-bold text-3xl">Fly It Anywhere</h2>
                <p class="lg:w-10/12  text-xl lg:text-2xl font-[gotham-light] font-[400]">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse et lacus suscipit ex ultrices lobortis. Nullam eget tellus ut massa.</p>

                <div class="bordr-2 border-[teal] w-full flex justify-end font-[gotham-bold]">
                    See More
                </div>

                    <div class="w-full flex flex-col lg:flex-row gap-2  lg:space-x-4">
                        <img src="~/assets/images/drone2.svg" class="object-cover w-full"/>

                        <img src="~/assets/images/drone3.svg" class="object-cover w-full"/>

                        <img src="~/assets/images/drone4.svg" class="object-cover w-full"/>
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
