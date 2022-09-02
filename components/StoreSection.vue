<template>
    <div class="h-screen w-full flex flex-col mt-[35rem] ">
        <h2 class="text-[gotham-bold] text-center text-4xl mb-[4rem]">DROVES</h2>

        <div class="grid ">
            <div class="w-auto shadow-2xl ">
                <img src="~/assets/images/drone5.svg" class="cover-image">
                <div class="py-8 pl-4">
                <p class="text-3xl font-bold font-[gotham-bold]">Mount Series 1</p>
                <p class="font-[gotham-light]">$299.99</p>
                </div>
            </div>
            

            <div class="w-auto shadow-2xl">
                <img src="~/assets/images/drone6.svg" class="cover-image">
                <div class="py-8 pl-4">
                <p class="text-3xl font-bold font-[gotham-bold]"> Valley Series 1</p>
                <p class="font-[gotham-light]">$249.99</p>
                </div>  
</div>

<div class="w-auto shadow-2xl">
    <img src="~/assets/images/drone7.svg" class="cover-image">
    <div class="py-8 pl-4">
    <p class="text-3xl font-bold font-[gotham-bold]">Droves Series 1</p>
    <p class="font-[gotham-light]">$199.99</p>
    </div>
</div>
        </div>

        <ShopBanner />
        <Footer />
    </div>
</template>


<style scoped>
 .grid {
        grid-template-columns: repeat(auto-fit, minmax(22.2rem, 1fr));
        gap: 3rem;
        padding-left:5%;
        padding-right:5%;
    }

    .cover-image {
        width: 100%;
        margin: 0 auto;
        max-width: 100%;
        object-fit: cover;
        
    }

</style>