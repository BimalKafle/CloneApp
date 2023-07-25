<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Navbar from '@/Layouts/NavbarLayout.vue'
import CheckCircle from 'vue-material-design-icons/CheckCircle.vue'
import ThumbUpOutline from 'vue-material-design-icons/ThumbUpOutline.vue'
import ThumbDownOutline from 'vue-material-design-icons/ThumbDownOutline.vue'
import RecommendedVideos from '@/Components/RecommendedVideos.vue'

// defineProps({
//     canLogin: Boolean,
//     canRegister: Boolean,
//     laravelVersion: String,
//     phpVersion: String,
// });
</script>

<template>
    <Head title="Youtube" />
    <Navbar>
            <div class="xl:flex">
                <div class="p-3">
                    <video src="/videos/sunset.mp4" controls autoplay></video>
                    <div class="text-white font-extrabold mt-4 text-2xl">
                        A cools
                    </div>
                    <div class="flex items-center mb-4">
                         
                    <img 
                        class="rounded-full m-1.5 mt-2 flex items-baseline w-8 h-8"
                    :src="`https://picsum.photos/id/${(Math.random()*100).toFixed(0)}/100`||''">
             
                        <div class="pl-2  mt-1">
                        
                            <div class=" text-white text-lg font-extrabold flex  items-center ">
                                Bimal Kafle <CheckCircle fillColor="#888888" :size="17"/>
                            </div>
                            <div class="text-sm text-gray-400 font-extrabold">1k Views - 3 days ago</div>
                        </div>
                    </div>

                    <div class="bg-[#3F3F3F] rounded-lg w-full p-3 text-white">
                        <div class="text-white text-lg font-extrabold">
                            1k views - 3 days ago
                        </div>
                        <div class="text-sm font-extrabold mb-6">
                            Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                        </div>
                         <div class="text-sm font-extrabold ">
                            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laudantium reprehenderit, quia consequuntur voluptate atque officia recusandae ratione ab illum. Consequuntur vitae ipsum accusantium soluta, fugiat aut fuga veniam delectus animi!
                        </div>
                    </div>

                    <div class="mt-6">
                        <div class="text-white text-lg font-extrabold">
                            20 Comments
                        </div>
                        <div class="flex items-flex mb-4 mt-2">
                             <img 
                        class="rounded-full mt-2 w-12 h-12"
                    :src="`https://picsum.photos/id/${(Math.random()*100).toFixed(0)}/100`||''" />
                        <div class="pl-6 mt-1">
                            <div class="text-white font-extrabold flex items-baseline">
                                     <div >
                                        Rajesh Hamal
                                    </div>
                                    <div class="text-gray-400 pl-3">
                                        6 days ago.
                                    </div>
                            </div>
                             <div class="text-gray-200 text-sm font-semibold">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro ea vitae alias veniam officia pariatur nemo delectus, quibusdam, reiciendis cumque rerum aut cupiditate tenetur, similique dolorem ipsam nostrum repellat ipsum.
                            </div>
                            <div class="mt-4 flex items-center">
                                <ThumbUpOutline fillColor="#FFFFFF" :size="20n" class="pr-2"/>
                                <div class="text-gray-400 text-sm font-extrabold pr-10">
                                        {{(Math.random()*100).toFixed(0)}}
                                </div>
                                <ThumbDownOutline fillColor="#FFFFFF" :size="20"  />
                            </div>
                        </div>
                          
                        </div>
                    </div>
                    
                </div>
                
                  <div class="w-[500px] p-3 sm:block hidden mt-11">
                  <div class="flex mb-3 ">
                    <RecommendedVideos
                    :vid="{
                      title:'little dog in a jumper',
                      video:'/videos/sunset.mp4',  
                      thumbnail:'/videos/Thumbnails/sunset.png',
                      user:'John Weeks Dev',
                      views:'12k views - 3 days ago',

                    }"
                   />
                  </div>
                </div>
            </div>
          
    </Navbar>

</template>

<style>

</style>
