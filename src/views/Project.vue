<script setup>
import project_items from '@/helpers/Project.json'

// project_items.forEach(item => {
//   item.items = item.items.map(path =>
//     new URL(`../${path}`, import.meta.url).href
//   )
// })

</script>
<template> 
    <div class="sm:h-auto grid grid-cols-1 place-items-center">
        <div class="text-center"> 
            <div class="xs:text-center sm:text-center md:text-start m-12"> 
                <h4 class="xs:text-3xl sm:text-3xl md:text-4xl font-medium"> PROJECT </h4>
                <p class="py-4 xs:text-sm sm:text-sm md:text-base font-normal"> 
                    This is a collection of all my personal projects, where I’ve explored various aspects of software development. From building web application to desktop and mobile application.
                    Each project reflects my passion for problem-solving and my continuous journey to improve as a software developer.
                </p>
                <div class="xs:grid xs:grid-cols-1 sm:grid sm:grid-cols-1 md:grid md:grid-cols-2 lg:grid lg:grid-cols-3 gap-8 mt-12"> 
                    <div v-for="(item, key) in project_items" :key="key" class="justify-start">
                        <div class="bg-cover overflow-hidden border"> 
                            <img :src="item.items[0]"  class="border transform transition duration-1200 hover:scale-110 cursor-pointer"/>
                        </div>
                        <div class="mt-7"> 
                            <p class="xs:text-sm sm:text-sm md:text-sm lg:text-lg font-semibold text-secondary"> {{ item.year }} </p>
                            <p class="xs:text-lg sm:text-lg lg:text-xl font-bold pt-2"> {{ item.text_title }} </p>
                            <p class="xs:text-sm sm:text-sm md:text-sm lg:text-lg pt-2"> {{ item.text_desc }} </p>
                        </div>
                    </div>
                </div>
            </div>    
        </div>
    </div>
</template>