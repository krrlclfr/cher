<script setup> 
import skills from '../helpers/Skills.json'
</script>
<template> 
    <div class="bg-[#0f1923] xs:h-auto sm:h-auto md:h-auto grid grid-cols-1 place-items-center xs:py-12 sm:py-12">
        <div class="text-center"> 
            <div class="xs:text-center sm:text-center md:text-start my-6 text-white"> 
                <h4 class="xs:text-3xl sm:text-3xl md:text-4xl font-medium"> SKILLS </h4>
                <p class="py-4 xs:text-sm sm:text-sm md:text-base font-normal"> Programming Languages and Tools i used for building web and mobile application. </p>
            </div>
            <div class="xs:grid xs:grid-cols-2 sm:grid sm:grid-cols-3 md:grid md:grid-cols-4 gap-6">
                <div v-for="(item, key) in skills" :key="key" class="flex justify-center"> 
                    <div class="bg-white h-32 w-40 rounded-md cursor-pointer hover:bg-slate-200">
                        <div class="h-4/6 grid place-items-center">
                            <i :class="item.icon" class="skills-icon"></i>
                        </div>
                        <div class="font-normal text-base"> 
                            {{ item.name }}
                        </div> 
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>