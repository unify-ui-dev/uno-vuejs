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
        href:"https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&display=swap",
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

</script>
<template>
    <header
        class="absolute left-0 top-0 w-full flex items-center h24 z40">
        <nav px="5 sm:10 md:12 lg:5"
            class="relative mx-auto lg-max-w-7xl w-full flex gap-x-5 justify-between items-center">
            <div class="flex items-center min-w-max relative">
                <router-link to="#" class="font-semibold flex items-center gap-x-2">
                    <div class="flex items-center -space-x-3">
                        <span bg="blue-6 dark:blue-5" class="h6 aspect-square rd-full flex"></span>
                        <span bg="pink-6 dark:pink-4" class="h6 aspect-square blur rd-full flex"></span>
                    </div>
                    <span text="lg gray-7 dark:gray-3">Agency</span>
                </router-link>
            </div>

            <div bg="white dark:gray-950 lg:!transparent" py="32 lg:0" px="5 sm:10 md:12 lg:0"
                class="fixed inset-x-0 h-100dvh lg-h-max top-0 left-0 w-full lg-top-0 lg-relative  lg-flex lg-justify-between duration-300 ease-linear"
                :class="navIsOpen ? '-translate-y-0 op100 visible' : '-translate-y-10 op-0 invisible lg-visible  lg-translate-y-0 lg-op-100'">
                <ul text="gray-7 dark:gray-3"
                    class="flex flex-col lg-flex-row gap-6 lg-items-center lg-w-full lg-justify-center">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <router-link :to="navItem.href" class="py2.5 duration-300 ease-linear hover-text-blue-6">
                            {{navItem.text}}
                        </router-link>
                    </li>
                </ul>
                <div
                    class="flex flex-col sm-flex-row sm-items-center gap-4  lg-min-w-max mt-10 lg-mt-0">
                    <router-link to="#" 
                        class="px6 py3 duration-300 ease-linear flex justify-center w-full sm-w-auto rd-xl text-blue-6 hover-text-white dark-text-white bg-hover-blue-7 dark-bg-gray-900 dark-hover-bg-ray-950 border border-blue-6 dark-border-gray-8">
                        Get It touch
                    </router-link>
                </div>
            </div>
            <div class="flex items-center lg-hidden">
                <button @click="toggleNavBar()" aria-label="toggle navbar" border-l="~ blue-1 dark:l-gray-8"
                    class="outline-none pl-3 relative py3 bg-transparent">
                    <div aria-hidden="true" bg="gray-8 dark:gray-3"
                        class="h0.5 w6 rd transition duration-300" :class="navIsOpen ? 'rotate-45 translate-y-1.5' : ''">
                    </div>
                    <div iaria-hidden="true" rd bg="gray-8 dark:gray-3"
                        class="mt2 h0.5 w6 transition duration-300" :class="navIsOpen ? '-rotate-45 -translate-y-1.5' : ''"></div>
                </button>
            </div>
        </nav>
    </header>

    <section class="min-h-max bg-blue-50 dark-bg-gray-950">
        <div class="absolute top-0 inset-x-0 h-64 flex items-start">
            <div
                class="h24 w-2/3 bg-gradient-to-br from-blue-5 op-20 blur-2xl dark-from-[#170cac] dark-invisible dark-op-40">
            </div>
            <div
                class="h20 w-3/5 bg-gradient-to-r from-[#4232ce] op-40 blur-2xl dark-from-[#670ccf] dark-op-40">
            </div>
        </div>
        <div class="min-h-100dvh w-full flex items-center relative">
            <div class="absolute top-1/2 left-1/2 -translate-y-1/2 -translate-x-1/2 w-2/5 aspect-[2/0.5] bg-gradient-to-br from-blue-6 to-pink-4 rd-full op-50 blur-2xl"></div>
            <div px="5 sm:10 md:12 lg:5" class="relative mx-auto pt32 lg-max-w-7xl w-full text-center space-y-10">
                <h1 un-text="gray-9 dark:white 4xl/tight sm:5xl/tight lg:6xl/tight xl:7xl/tight" class="mx-auto max-w-4xl font-bold">
                    We help you to grow your business
                </h1>
                <p text="gray-7 dark:gray-3" class="mx-auto max-w-2xl">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt saepe atque enim quasi a ipsum asperiores necessitatibus deleniti, sint quo vel corporis dignissimos
                </p>
                <div class="flex sm-flex-row flex-col gap-5 w-full mx-auto max-w-xl">
                    <form action="#" text="gray-6 dark:gray-4" bg="gray-1 dark:gray-9 focus-within:white dark:focus-within:gray-950" border="~ gray-2 dark:gray-8 focus-within:blue-6" shadow="lg gray-2/20 dark:transparent"
                        class="py1 pl6 w-full pr1 flex gap-3 items-center
                            rd-xl ease-linear">
                        <span class="min-w-max pr2 border-r border-gray-2 dark-border-gray-8">
                            <span i-carbon-email flex text-2xl></span>
                        </span>
                        <input type="email" name="" id="" placeholder="johndoe@gmail.com"
                            class="w-full py3 outline-none bg-transparent">
                        <button un-after="absolute content-empty inset-x-0 aspect-square scale-0 op-70 origin-center duration-300 ease-linear top-0 left-0 bg-[#172554] hover:op-100 hover:scale-[2.5]"
                                border="~ transparent hover:[#172554]"
                                class="flex text-white justify-center items-center w-max min-w-max sm-w-max px6 h12 rd-lg outline-none relative
                                overflow-hidden duration-300 ease-linear bg-blue-6">
                            <span class="hidden sm-flex relative z-[5]">
                                Get in touch
                            </span>
                            <span class="flex sm-hidden relative z-[5]">
                                <span i-carbon-send text-xl flex></span>
                            </span>
                        </button>
                    </form>
                </div>
                <div class="flex items-center gap-1 mt-10 justify-center gap-x-3">
                    <div class="flex items-center -space-x-2 " un-children="rd-full ring-4 ring-white dark:ring-gray-950 w-10 h-10 object-cover">
                        <img src="/images/podCast.webp" width="2250" alt="listener avatar">
                        <img src="/images/podCast.webp" width="2250" alt="listener avatar">
                        <img src="/images/podCast.webp" width="2250" alt="listener avatar">
                    </div>
                    <div class="flex flex-col justify-start items-start">
                        <span text="lg gray-8 dark:gray-2" class="font-semibold">+12k</span>
                        <span text="sm gray-6 dark:gray-3">WordWide Customers</span>
                    </div>
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