<script setup>
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3';
import MenuIcon from 'vue-material-design-icons/Menu.vue'
import Magnify from 'vue-material-design-icons/Magnify.vue'
import SideNavItems from '@/Components/SideNavItems.vue';
const showingNavigationDropdown = ref(false);
let openSideNav=ref(true)
</script>

<template>
 <div class="relative">
    <div id="topNav"  class="w-[100%] h-[60px] fixed bg-black z-20 flex items-center justify-between">
        <div class="flex items-center">
            <button @click="openSideNav=!openSideNav" class="p-2 ml-3 rounded-full hover:bg-grey-800 inline-block cursor-pointer">
                <MenuIcon fillColor="#ffffff" :size="26"/>
            </button>
            <div class="mx-2"></div>
            <div class="flex text-white items-center justify-center mr-10 cursor-pointer">
                Youtube
            </div>
        </div>
        <div class="w-[600px] md:block hidden">
            <div class="rounded-full flex items-center bg-[#222222]">
                <input type="text"
                class="
                    form-control
                    block
                    w-full
                    px-5
                    py-1.5
                    text-base
                    font-normal
                    text-gray-200
                    bg-black
                    placeholder-gray-400
                    bg-clip-padding
                    border
                    border-solid
                    border-l-gray-700
                    border-y-gray-700
                    rounded-l-full
                    transition
                    ease-in-out
                    m-0
                    border-transparent
                    focus-ring-0
                "
                placeholder="Search"
                />
                <Magnify class="mx-6" fillColor="#FFFFFF" :size="23"/>
            </div>
        </div>
        <div>
            <img class="rounded-full mx-8" width="35" src="https://yt3.ggpht.com/yti/AOXPAcUTaWEZsJulLKUCVmCbFAURy0056Rv-59UhwE0QHg=s88-c-k-c0x00ffffff-no-rj" >
        </div>
    </div>
    <div id="sideNav"
     class="h-[100%] fixed z-0 bg-black "
     :class="[!openSideNav?'w-[70px]':'w-[240px]']"
     >
        <ul 
        :class="[!openSideNav?'p-2':'px-5 pb-2 pt-[7px]']"
        class="mt-[60px] w-full">
            <SideNavItems :openSideNav="openSideNav" iconString='Home'/>
            <SideNavItems :openSideNav="openSideNav" iconString='Add Vedio'/>
            <SideNavItems :openSideNav="openSideNav" iconString='Delete Vedio'/>
            <div class="border-b border-b-gray-700 my-2.5"></div>
            <SideNavItems :openSideNav="openSideNav" iconString='Subscriptions'/>
            <SideNavItems :openSideNav="openSideNav" iconString='Library'/>
            <SideNavItems :openSideNav="openSideNav" iconString='Liked'/>
            <SideNavItems :openSideNav="openSideNav" iconString='Watch Later'/>
            <SideNavItems :openSideNav="openSideNav" iconString='History'/>
            <div v-if="openSideNav">
                <div class="border-b border-b-gray-700 my-2.5"></div>
                   <div class="text-gray-400 text-[14px] text-extrabold">
                About Press Copyright
                <div>Contact Us</div>
                Creator Advertise Developers
            </div>
             <div class="border-b border-b-gray-700 my-2.5"></div>
             <div class="text-gray-400 text-[14px] text-extrabold">
                Terms Privacy Policy & Safety
                <div>How Youtube Works</div>
                <span>Test New Features</span>
                
            </div>
             <div class="border-b border-b-gray-700 my-2.5"></div>
            </div>
         
        </ul>
    </div>
    <div id="sideNavOverlay"></div>

    <div
        class="w-[100%] h-[calc(100vh-60vh) absolute right-0 top-[60px]]"
        :class="{
            'w-[calc(100%-60px)]':!openSideNav,
            'w-[calc(100%-240px)]':openSideNav,

        }"
    >

        <slot/>
    </div>
    
 </div>
</template>

<style >
body{
    background: black;
}
</style>