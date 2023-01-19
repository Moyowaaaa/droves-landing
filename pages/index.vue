<template>

	<div class="" v-if="assetsLoaded">
		<Main />
		 <AboutSection/>
		<StoreSection />
		

	</div>
	
</template>

<script setup lang="ts">
import mainBackground from '../assets/images/mainbackground.png'
import mainDrone from '../assets/images/main.svg'
import tooltip from '~/assets/images/tooltip.svg'
import gothamBlack from '../assets/fonts/Gotham-Black.otf'
import gothamLight from '../assets/fonts/GothamLight.otf'
import gothamMedium from '../assets/fonts/GothamMedium.otf'
import gothamBold from '../assets/fonts/GothamBold.otf'
import { resolve } from 'path'

const assetsLoaded = ref<boolean>(false)

const assets = ref([mainDrone,tooltip, mainBackground])


onMounted(() => {
	const promises:any[] = []
    assets.value.forEach(asset => {
        const img = new Image()
        img.src = asset
        promises.push(new Promise((resolve, reject) => {
          img.onload = resolve
          img.onerror = reject
        }))   
		new Promise((resolve,reject) => {
		const font1 = new FontFace('gotham-black',`url(${gothamBlack})`);
            font1.load().then(resolve,reject)
			const font2 = new FontFace('gotham-light',`url(${gothamLight})`);
            font2.load().then(resolve,reject)
			const font3 = new FontFace('gotham-md',`url(${gothamMedium})`);
            font3.load().then(resolve,reject)
			const font4 = new FontFace('gotham-bold',`url(${gothamBold})`);
            font4.load().then(resolve,reject)

			
		})     
    })
        
    Promise.all(promises).then(() => {
        assetsLoaded.value = true
      })

})

</script>

<style scoped>

</style>
