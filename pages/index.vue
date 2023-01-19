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
    })
        
    Promise.all(promises).then(() => {
        assetsLoaded.value = true
      })

})

</script>

<style scoped>

</style>
