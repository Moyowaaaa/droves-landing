<template>
    <div class="banner">
        <div class="w-full h-full flex">

            <!-- <h1 class=" font-bold font-[gotham-bold] text-white">4K</h1> -->

            <div class="flex justify-between w-full h-full items-center ">
                <img src="~/assets/images/4ktext.svg"/>

                <div class="flex flex-col gap-6 pr-32">
                <div class="flex ">
                    <img src="~/assets/images/outline1.svg"/>
                    <p class="font-[gotham-light] text-white">Still Image Resolution 60fps</p>
                </div>

                <div class="flex">
                    <img src="~/assets/images/outline2.svg"/>
                    <p class="font-[gotham-light] text-white">Video resolution 4k</p>
                </div>


                <div class="flex">
                    <img src="~/assets/images/outline3.svg"/>
                    <p class="font-[gotham-light] text-white">Recording at 100Mbps bitrate</p>
                </div>



            </div>

            </div>
           
        </div>
    </div>
</template>



<style scoped>
    .banner{
        background-image:url('../assets/images/4k.svg');
        background-size:cover;
        padding-top:5%;
        padding-bottom:5%;
        margin-top:10%;
        margin-bottom: 10%;
        
        
    }

    
    </style>