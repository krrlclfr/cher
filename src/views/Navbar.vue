<script setup> 
import Nav from '../helpers/Navbar.json'
import { ref } from 'vue'

const is_open_menu = ref(false)

function openMenu() {
    is_open_menu.value = !is_open_menu.value
}

function closeMenu() {
    is_open_menu.value = false
}
</script>
<template> 
    <div class="relative :container bg-[#111111] h-20 text-white flex lg:justify-start xs:justify-between place-items-center">
        <div class="mx-12"> 
            <img src="@/assets/cher-logo.png" width="50"/>
        </div>
        <div class="xs:invisible sm:invisible md:invisible lg:visible lg:flex lg:flex-row gap-x-1">
            <div v-for="(item, key) in Nav" :key="key" class="cursor-pointer font-medium rounded-md py-2 pb-2 hover:text-[#ff4655] hover:bg-[#2b2a28]"> 
                <a :href="`#${item.link}`">
                    <p class="px-7"> 
                        {{ item.link }} 
                    </p>
                </a>
            </div> 
        </div>
        <div class="xs:visible sm:visible md:visible lg:invisible justify-end text-white mx-12"> 
            <button @click="openMenu"> 
                <i class="fas fa-bars"></i>
            </button>
        </div>
        <div v-if="is_open_menu" class="lg:invisible "> 
            <div class=":container flex flex-row absolute h-screen w-screen top-0 right-0 z-20 transition delay-700 duration-700 ease-in-out"> 
                <div class="bg-zinc-950 w-2/5 opacity-70"> </div>
                <div class="container h-full w-full px-6 bg-[#1f1f1f] opacity-100"> 
                    <div class="flex justify-between place-items-center h-20">
                        <div class="ml-6"> 
                            <img src="@/assets/cher-logo.png" width="50"/>
                        </div> 
                        <div> 
                            <button @click="closeMenu" class="mr-6">
                                <i class="fas fa-times"></i>
                            </button>
                        </div>
                    </div>
                    <div v-for="(item, key) in Nav" :key="key" class="cursor-pointer font-medium rounded-md py-2 pb-2 hover:text-[#ff4655] hover:bg-[#2b2a28]"> 
                        <p class="px-4 my-3"> 
                            {{ item.link }} 
                        </p>
                    </div>
                </div>
            </div> 
        </div>
    </div>
</template>