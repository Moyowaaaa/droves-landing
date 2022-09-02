<template>
    <div class="h-auto w-full flex flex-col ">

        <div class=" flex pt-16 gap-4 pl-20 pr-20 ">
            <img src="~/assets/images/drone1.svg">

            
            <div class="w-8/12   flex flex-col gap-4  justify-end">
                <h2 class="font-[gotham-bold] font-bold text-3xl">Fly It Anywhere</h2>
                <p class="w-9/12 text-2xl">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse et lacus suscipit ex ultrices lobortis. Nullam eget tellus ut massa.</p>

                <div class="flex gap-4 pr-12">
                    <img src="~/assets/images/drone2.svg" class="w-4/12"/>

                    <img src="~/assets/images/drone3.svg" class="w-4/12"/>

                    <img src="~/assets/images/drone4.svg" class="w-4/12"/>
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
.drone1{
    background: url('../assets/images/drone1.svg');
    background-size: cover;
    background-repeat: no-repeat;
}

</style>
