<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Navbar from '@/Layouts/NavbarLayout.vue'
import VideoCard from '@/Components/VideoCard.vue'
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
        <div class="grid 2xl:grid-cols-5 xl:grid-cols-4 lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-2">
            <VideoCard
                title="Beautiful Sunset"
                user="Bimal Kafle"
                views="23k views - 3 days ago"
                image="https://yt3.ggpht.com/yti/AOXPAcUTaWEZsJulLKUCVmCbFAURy0056Rv-59UhwE0QHg=s88-c-k-c0x00ffffff-no-rj"
                videoUrl="/videos/sunset.mp4"
                thumbnail="/videos/Thumbnails/sunset.png"

            />

        </div>
    </Navbar>

</template>

<style>

</style>
