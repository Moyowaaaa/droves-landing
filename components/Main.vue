<template>
    <div class="main h-screen">
        
        <div class=" w-full flex  h-full flex-col ">

            <Navbar />

            <div class="flex h-full h-full">
            <div class="w-8/12 h-full pl-20 flex flex-col gap-6 justify-center">
              <h1 class="text-7xl font-bold ">Fly With The Birds</h1>  
              
              
              <p class="font-normal text-2xl">Go beyond the mountains and into the valleys</p>

              <div class="flex gap-4">
                <button class="p-6 flex items-center justify-center bg-[black] text-[white] text-2xl">
                    Mount Series 1
                </button>

                <button class="p-6 flex items-center justify-center border-2 border-[black] text-2xl">
                    Valley Series 1
                </button>
              </div>
            </div>

            <div class="absolute right-48 top-24 h-4/6 w-[60vw] object-cover">
            <img src="~/assets/images/main.svg" class="h-full w-full object-cover">
        </div>
        </div>


        <div class="absolute fade pb-3">
            <h2 class="text-6xl font-black text-black">Droves</h2>
        </div>
        </div>

        </div>  

</template>

<script lang="ts">

</script>

<style scoped>
.main{
    background-color: white;
    background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-position-x: 125vh;
  width:100%;
  height:100vh;
  background-color: #f2eee6;
  background-attachment: fixed;
    background: linear-gradient(to bottom, transparent, transparent),url('../assets/images/mainbackground.png') ;

}
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
</style>