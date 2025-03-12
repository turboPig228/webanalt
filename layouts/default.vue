

<template>
    <header class = "flex flex-row w-full p-4 bg-gradient-to-r from-pink-800 to-pink-400 shadow-md shadow-pink-700">
        <div class = "basis-1/4 items-center justify-start px-4">
            <img src="assets/images/cry.jpg" class="w-20 h-20 rounded-full">
        </div>
        <div class = "basis-1/4">
        </div>
        <nav class = "basis-1/2 flex flex-row items-center justify-end px-4 gap-4">
            <NuxtLink to = "/" class = "my-auto p-2 hover:bg-red-500 rounded-md">Home</NuxtLink>
            <NuxtLink to = "/" class = "my-auto p-2 hover:bg-red-500 rounded-md">Lab3</NuxtLink>
            <NuxtLink to = "#"class = "my-auto p-2 hover:bg-red-500 rounded-md">LogIn</NuxtLink>
            <NuxtLink to = "#"class = "my-auto p-2 hover:bg-red-500 rounded-md">LogOut</NuxtLink>
        </nav>
    </header>

    <main class= "p-5 flex bg-pink-200 h-screen">
        <slot />
    </main>

    <footer class = "flex flex-row w-full bg-gradient-to-r from-pink-400 to-pink-800 border-purple-400 items-center justify-center px-4 py-2 gap-4">
        <a href="https://www.youtube.com/"><img src="assets/images/Youtube_logo.png" class = "w-16 h-16"></a>
        <a href="https://github.com/"><img src="assets/images/github.png" class = "w-16 h-16"></a>
        <a href="https:www.facebook.com/"><img src="assets/images/Facebook.png" class = "w-16 h-16"></a>
    </footer>
</template>

<script setup>
import { useHead} from '#app';

useHead({
    script: [
    {
        asyns: true,
        src: 'https://www.googletagmanager.com/gtag/js?id=G-J7101YYK8R',
    },
    {
        innerHTML: `
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'G-J7101YYK8R')
    `,
    type: 'text/javascript',
    },    
    ],
    __dangerouslyDisableSanitizersByTagID: {
        gtab: ['innerHTML'],
    }
});
</script>