<script setup>
import { useHead } from 'unhead'
import { ref } from 'vue'

const navIsOpen = ref(false)
useHead({
  title: 'SaaS Herosection',
  meta: [
    {
      name: 'description',
      content: 'My page description',
    },
  ],
  link:[
    {
        href:"https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap",
        rel:"stylesheet"
    }
  ]
})

const navItems = [
    {
        id:1,
        text:"Solutions",
        href:"#"
    },
    {
        id:2,
        text:"Company",
        href:"#"
    },
    {
        id:3,
        text:"Plateforme",
        href:"#"
    },
    {
        id:4,
        text:"Ressources",
        href:"#"
    },
    {
        id:5,
        text:"Contact",
        href:"#"
    }
]

function toggleNavBar(){
    navIsOpen.value = !navIsOpen.value
    document.body.classList.toggle("overflow-y-auto")
}

function closeNavBar(){
    navIsOpen.value = false
    document.body.classList.add("overflow-y-auto")
}
</script>
<template>
    <div @click="closeNavBar()" aria-hidden="true" class="fixed bg-gray-8/40 inset-0 z-30" :class="navIsOpen ? 'flex lg-hidden' : 'hidden'"></div>
    <header sticky top-0 w-full flex items-center h20 z40 border-b="~ gray-1 dark:gray-9"
        bg="white/80 dark:gray-950/80" backdrop-filter backdrop-blur-xl>
        <nav px="5 sm:10 md:12 lg:5" relative mx-auto max-w-7xl w-full flex gap-x-5 justify-between items-center>
            <div class="flex items-center min-w-max">
                <router-link to="#" class="text-xl font-semibold text-gray-7 flex items-center gap-x-2">
                    <span class="flex">
                        <span class="w3 h6 rd-l-full flex bg-blue-6"></span>
                        <span class="w3 h6 rd-r-full flex bg-teal-4 mt2"></span>
                    </span>
                    <span text="lg gray-7 dark:gray-300">skySoft</span>
                </router-link>
            </div>

            <div top-20 lg-top-0 left-0 bg="white dark:gray-950 lg:transparent"
                border-b="~ gray-2 dark:gray-8 lg:none" py="8 lg:0" px="5 sm:10 md:12 lg:0" w-full fixed lg-relative
                lg-flex gap-6 lg-justify-between duration-300 ease-linear
                :class="navIsOpen ? 'translate-y-0 op100 visible':'translate-y-10 op0 invisible lg-visible  lg-translate-y-0 lg-op100'">
                <ul text="gray-7 dark:gray-300" flex flex-col gap-6 lg="flex-row items-center w-full justify-center">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <router-link :to="navItem.href" class="py2.5 duration-300 ease-linear hover-text-blue-6">
                            {{navItem.text}}
                        </router-link>
                    </li>
                </ul>
                <div mt="10 lg:0"
                    class="flex flex-col sm-flex-row sm-items-center gap-4 lg-min-w-max">
                    <router-link to="#" 
                        class="px6 py3 duration-300 ease-linear flex justify-center w-full sm-w-auto rd-full border order-blue-6 dark-border-gray-8 text-blue-6 hover-text-white dark-text-white
                        hover-bg-blue-7 dark-bg-gray-9 dark-bg-hover-gray-950">
                        Request trial
                    </router-link>
                </div>
            </div>
            <div class="flex items-center lg-hidden">
                <button @click="toggleNavBar()" aria-label="toggle navbar" border-l="~ gray-3 dark:gray-7"
                    class="outline-none pl3 relative py3 bg-transparent">
                    <div aria-hidden="true" bg="gray-7 dark:gray-3"
                        class="h0.5 w6 rd transition duration-300" :class="navIsOpen ? 'rotate-45 translate-y-1.5' :''">
                    </div>
                    <div aria-hidden="true" bg="gray-7 dark:gray-3"
                        class="mt2 h0.5 w6 rd transition duration-300" :class="navIsOpen ? '-rotate-45 -translate-y-1.5' :''"></div>
                </button>
            </div>
        </nav>
    </header>

    <section lg-min-h-max bg="blue-50 dark:gray-950">
        <div
            class="absolute left-0 top-20 w40 aspect-video bg-gradient-to-br from-blue-6 to-sky-4 rd-full blur-3xl op60">
        </div>
        <div p="x5 sm:x10 md:x12 lg:x5 y24 lg:y4 lg:b6"
                class="relative mx-auto max-w-7xl w-full flex flex-col lg-flex-row lg-items-stretch gap-10">
                <div text="center lg:left" class="lg-w-1/2 max-w-2xl md-max-w-3xl mx-auto flex flex-col md-justify-center">
                    <h1 text="teal-950 dark:white 4xl md:5xl lg:6xl" font="semibold display">
                        Manage with better
                        <span
                            class="bg-clip-text text-transparent bg-gradient-to-br from-teal-6 to-blue-6">experience</span>
                        your Studio!
                    </h1>
                    <p text="gray-7 dark:gray-3" mt9 mx-auto lg-mx-0 max-w-xl>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum, beatae omnis ipsa magnam neque ut
                    </p>
                    <div class="mt9 flex flex-col sm-flex-row justify-center lg-justify-start gap-4">
                        <a href="#"
                            class="flex items-center justify-center py-3 px-6 shadow-lg bg-blue-6 transition ease-linear hover-bg-blue-8 active-bg-blue-7 text-white rd-full">
                            Get Started
                        </a>
                    </div>
                    <div class="flex items-center gap-1 gap-x-2 mt9 justify-center lg-justify-start py5">
                        <div class="flex items-center -space-x-2">
                            <img src="/images/podCast.webp" width="2250" alt="listener avatar"
                                class="w10 h10 object-cover rd-full ring-4 ring-white dark-ring-gray-950">
                            <img src="/images/podCast.webp" width="2250" alt="listener avatar"
                                class="w10 h10 object-cover rd-full ring-4 ring-white dark-ring-gray-950">
                            <img src="/images/podCast.webp" width="2250" alt="listener avatar"
                                class="w10 h10 object-cover rd-full ring-4 ring-white dark-ring-gray-950">
                        </div>
                        <div class="flex flex-col justify-start items-start ">
                            <span text="lg gray-8 dark:gray-2" class="font-semibold">+12k</span>
                            <span text="sm gray-6 dark:gray-3">Lovely users</span>
                        </div>
                    </div>
                </div>
                <div class="lg-w1/2 relative lg-h-auto max-w-2xl md-max-w-3xl mx-auto hidden md-flex justify-end">
                    <div relative w-full h-full flex items-center aspect-square overflow-hidden lg-aspect-auto>
                        <img src="/images/woman-at-meet-up.webp" width="1266" height="1224" alt="woman at virtual meetup"
                            class="w-full relative hauto">
                    </div>
                </div>
            </div>
    </section>
</template>

<style >
body{
    --at-apply: font-poppins bg-white dark-bg-gray950
}
</style>