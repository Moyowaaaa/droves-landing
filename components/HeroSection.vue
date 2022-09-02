<template>
    <div class="h-auto w-full flex flex-col ">


        <div class="h-[600px] px-[5%] pt-16">
            <div class="w-full h-full flex gap-4 items-end">

                
                <div class="h-full w-5/12 ">
                    <img src="~/assets/images/drone1.svg " class="object-cover w-full h-full ">
                </div>


                <div class="  w-7/12 flex flex-col gap-4 ">

                 
                    <h2 class="font-[gotham-bold] font-bold text-3xl">Fly It Anywhere</h2>
                <p class="w-10/12 text-2xl font-[gotham-light] font-[400]">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse et lacus suscipit ex ultrices lobortis. Nullam eget tellus ut massa.</p>

                <div class="bordr-2 border-[teal] w-full flex justify-end font-[gotham-bold]">
                    See More
                </div>

                    <div class="w-full flex gap-2  space-x-4">
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

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup() {
        
    },
})
</script>

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
