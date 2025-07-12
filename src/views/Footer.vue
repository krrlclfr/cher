<script setup>
import social_media_icon from '@/helpers/Social_Media.json'
</script>
<template> 
    <div class=":container bg-[#111111] xs:h-auto sm:h-auto md:h-96 text-white xs:py-12 sm:py-12"> 
        <div class="xs:grid xs:grid-cols-1 sm:grid sm:grid-cols-1 md:grid md:grid-cols-3 place-content-center h-full"> 
            <div class="grid grid-cols-1 gap-4 place-items-center "> 
                <img src="@/assets/cher-logo.png" width="120"/>
            </div>
            <div class="text-center text-base xs:pt-12 sm:pt-12"> 
                <div class="xs:text-center sm:text-center md:text-start"> 
                    <p class="my-3 font-medium"> Portfolio </p>
                    <p class="my-3 font-medium"> <a href="#About" class="hover:text-[#ff4655] cursor-pointer"> About </a></p>
                    <p class="my-3 font-medium"> <a href="#Qualification" class="hover:text-[#ff4655] cursor-pointer"> Download Resume </a></p>
                    <p class="my-3 font-medium"> <a href="#Contact" class="hover:text-[#ff4655] cursor-pointer"> Contact Me </a></p>
                </div>
            </div>
            <div class="text-base xs:py-12 sm:py-12 xs:text-center sm:text-center md:text-start"> 
                <p class="my-3 font-medium"> Follow Me </p>
                <div class="flex flex-row xs:justify-center md:justify-start"> 
                    <div v-for="(item, key) in social_media_icon" :key="key" class="basis-9"> 
                        <a :href="item.link" target="_blank" class="hover:text-[#ff4655] cursor-pointer"> 
                            <i :class="item.icon" class="social-media-icon"> </i>
                        </a>
                    </div>
                </div>
                <p class="my-3 font-medium"> Archer Cabahug </p>
                <p class="my-3 font-medium"> @2024 </p>
            </div>
        </div>
    </div>
</template>