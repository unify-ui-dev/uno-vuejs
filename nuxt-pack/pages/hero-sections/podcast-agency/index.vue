<script setup>
const navIsOpen = useState('navIsOpen', ()=>false)
useHead({
  title: 'Podcast Herosection',
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
        text:"Podcast",
        href:"#"
    },
    {
        id:2,
        text:"Solutions",
        href:"#"
    },
    {
        id:3,
        text:"Blog",
        href:"#"
    },
    {
        id:4,
        text:"About",
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
    <header class="absolute inset-x-0 top-0 h20 flex items-center z50">
        <div px="5 sm:p10 md:12 lg:5" class="mx-auto max-w-7xl w-full relative z50">
            <nav class="flex items-center justify-between w-full relative">
                <div class="inline-flex relative bg-inherit">
                    <nuxt-link to="#" class="flex items-center gap-2">
                        <span class="flex">
                            <span class="w3 h6 rd-l-full flex bg-emerald-5"></span>
                            <span class="w3 h6 rd-r-full flex bg-[#f88fc2] mt2"></span>
                        </span>
                        <span class="text-lg text-gray-7 dark:text-white">Podux</span>
                    </nuxt-link>
                </div>
                <div data-navbar py="6 lg:0" lg-pt-0 px="5 sm:8 md:12 lg:0"
                    bg="white dark:gray-950 lg:transparent lg:dark:transparent"
                    shadow="lg gray-1 dark:transparent lg:none" border="1 gray-2 dark:gray-7 lg:none" absolute
                    top-10 flex flex-col lg="top-0 z-auto relative flex-row justify-between" rd="xl lg:none" w-full
                    transition-all duration-300 ease-linear origin-top
                    :class="navIsOpen ? 'visible op100 translate-y-0' : 'invisible op20 lg-op-100 translate-y-6 lg-visible lg-translate-y-0'">
                    <ul text="gray-7 dark:gray-1" gap="y-4 lg:x-8"
                        class="w-full flex lg-items-center flex-col lg-flex-row lg-w-full lg-justify-center">
                        <li v-for="navItem in navItems" :key="navItem.id">
                            <nuxt-link :to="navItem.href" class="transition hover-text-emerald-5 ease-linear">
                                {{navItem.text}}
                            </nuxt-link>
                        </li>
                    </ul>
                    <div mt="8 lg:0"
                        class="lg-min-w-max flex flex-col lg-flex-row lg-items-center gap-4 w-full sm-w-max">
                        <nuxt-link to="#"
                            class="px-7 relative text-emerald-5 h12 flex w-full sm-w-max justify-center items-center before-content-empty before-absolute before-inset-0 before-rd-full  before-bg-emerald-5/5 dark-before-bg-gray-5/10 before-transition-transform before-ease-linear hover-before-scale-105 active-before-scale-95">
                            <span class="relative">Signin</span>
                        </nuxt-link>

                        <nuxt-link to="#" class="px-7 relative text-white h-12 flex w-full sm-w-max justify-center items-center before-absolute before-content-empty before-inset-0 before-rd-full before-bg-emerald-5 before-transition-transform before-ease-linear hover-before-scale-105 active-before-scale-95">
                            <span class="relative"> Join Us</span>
                        </nuxt-link>
                    </div>
                </div>
                <div border-l="lg:~ lg:gray-1 dark:lg:gray-7" class="flex ml-2 pl-2 min-w-max items-center gap-x-3">
                    <button aria-label="toggle theme" text="gray-7 dark:gray-3"
                        class="outline-none flex relative p-3 bg-transparent">
                        <span i-carbon-moon text-xl bg="gray-7 dark:gray-3" hidden dark-flex></span>
                        <span i-carbon-sun text-xl bg="gray-7 dark:gray-3" flex dark-hidden></span>
                    </button>
                    <button aria-label="toggle navbar" @click="toggleNavBar()"
                        class="outline-none lg-hidden w7 hauto flex flex-col relative bg-transparent">
                        <span bg="gray-8 dark:gray-2"
                            class="w6 h0.5 rd-full transition-all duration-300 ease-linear" :class="navIsOpen ? 'scale-x-100 rotate-40 translate-y-0.375rem' : 'origin-right  scale-x-75'">
                        </span>
                        <span bg="gray-8 dark:gray-2"
                            class="w6 origin-center mt1 h0.5 rd-full transition-all duration-300 ease-linear" :class="navIsOpen ? 'scale-x-0 op0' : ''">
                        </span>
                        <span bg="gray-8 dark:gray-2"
                            class="w6 mt1 h0.5 rd-full transition-all duration-300 ease-linear" :class="navIsOpen ? 'origin-right scale-x-100 rotate-40 translate-y-0.150' : ' scale-x-50'">
                        </span>
                    </button>
                </div>
            </nav>
        </div>
    </header>

    <section class="relative w-full">
        <div class="absolute top-0 inset-x-0 h64 flex items-start">
            <div
                class="h24 w2/3 bg-gradient-to-br from-emerald-5 op20 blur-2xl dark-from-[#570cac] dark-invisible dark-op-40">
            </div>
            <div
                class="h20 w3/5 bg-gradient-to-r from-[#8cd66a] op40 blur-2xl dark-from-[#670ccf] dark-op-40">
            </div>
        </div>
        <div px="5 sm:p10 md:12 lg:5" class="mx-auto max-w-7xl w-full relative"><!--[-->
            <div aria-hidden="true" class="absolute inset-y-0 w-44 left-0 hidden dark-flex">
                <div
                    class="h-full md-h-1/2 lg-h-full w-full bg-gradient-to-tr op-40 dark-blur-2xl dark-from-[#570cac] dark-op-20">
                </div>
            </div>
            <div
                class="grid lg-grid-cols-2 gap-10 xl-gap-14 relative pt24 lg-max-w-none max-w-2xl md-max-w-4xl mx-auto">
                <div class="lg-py-6">
                    <div text="center lg:left">
                        <span bg="gray-1 dark:gray-9" text-gray-8 dark-text-gray-2 px2 py1 rd-md>
                            New season available <nuxt-link to="#" class="underline text-emerald-7 dark-text-white font-semibold">here</nuxt-link>
                        </span>
                        <h1 text="gray-7 dark:white 4xl md:5xl xl:6xl" class="pt-8 font-bold">
                            Find and listen <br> Favorite
                            <span class="text-transparent bg-clip-text bg-gradient-to-br from-emerald-5 to-[#8cd66a]">
                                Podcast
                            </span>
                            on internet
                        </h1>
                    </div>

                    <p text="gray-7 dark:gray-3 center lg:left" class="mt8 mx-auto max-w-lg lg-max-w-md lg-mx-0">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum, beatae omnis ipsa magnam neque
                        ut nam
                        nesciunt esse fugit praesentium hic magni possimus illo consequatur.
                    </p>

                    <div class="flex items-center gap-4 mt8 flex-col sm-flex-row sm-w-max sm-mx-auto lg-mx0">
                        <nuxt-link to="#" class="px-7 relative text-white h-12 flex w-full sm-w-max justify-center items-center before-absolute before-content-empty before-inset-0 before-rd-full before-bg-emerald-5 before-transition-transform before-ease-linear hover-before-scale-105 active-before-scale-95">
                            <span class="relative"> Join Us</span>
                        </nuxt-link>
                        <nuxt-link to="#"
                            class="px-7 relative text-emerald-5 h12 flex w-full sm-w-max justify-center items-center before-content-empty before-absolute before-inset-0 before-rd-full  before-bg-emerald-5/5 dark-before-bg-gray-5/10 before-transition-transform before-ease-linear hover-before-scale-105 active-before-scale-95">
                            <span class="relative">Listening Episode</span>
                        </nuxt-link>
                    </div>

                    <div
                        class="flex items-center text-center flex-col sm-flex-row gap-4 sm:gap-0 mt8 w-max mx-auto lg-mx-0">
                        <div class="flex items-center -space-x-2">
                            <img src="/images/sidebiew.webp" width="1240" alt="avatar"
                                class="w10 h10 rd-full ring-4 ring-white dark-ring-gray-950 object-cover">
                            <img src="/images/sidebiew.webp" width="1240" alt="avatar"
                                class="w10 h10 rd-full ring-4 ring-white dark-ring-gray-950 object-cover">
                            <img src="/images/sidebiew.webp" width="1240" alt="avatar"
                                class="w10 h10 rd-full ring-4 ring-white dark-ring-gray-950 object-cover">
                            <img src="/images/sidebiew.webp" width="1240" alt="avatar"
                                class="w10 h10 rd-full ring-4 ring-white dark-ring-gray-950 object-cover">
                            <span bg="gray-2 dark:gray-8" text="xs gray-7 dark:gray-3" ring="4 white dark:gray-950"
                                class="w10 h10 rd-full flex items-center justify-center">
                                300+
                            </span>
                        </div>
                        <span class="pl2 text-gray-6 dark-text-gray-2"> WordWide listners </span>
                    </div>
                </div>
                <div class="lg-h-full hidden md-flex">
                    <div
                        class="flex w-full h96 min-h-[24rem] lg-min-h-[none] lg-w-full lg-h-full items-center relative">
                        <div
                            class="absolute z-0 top-1/2 -translate-y-1/2 w-5/6 right-0 h-[calc(80%+20px)] bg-gradient-to-tr op25 from-emerald-5 to-pink-300 dark-from-[#570cac] dark-to-emerald-5 blur-2xl">
                        </div>
                        <div  bg="white dark:gray-950"  shadow="lg gray-1 dark:transparent"  border="~ gray-2 dark:gray-8"
                            class="absolute w-3/5 h-full z10 p1 -translate-y-1/2 top-1/2 right-3 rd-3xl">
                            <img src="/images/sidebiew.webp" alt="In studio" width="500" height="auto" loading="lazy"
                                class="w-full h-full rd-2xl object-cover">
                        </div>
                        <div bg="white dark:gray-950"  shadow="lg gray-1 dark:transparent"  border="~ gray-2 dark:gray-8" 
                            class="absolute -translate-y-1/2 top-1/2 h-[calc(80%-2rem)] w-[calc(40%-20px)] p1 rd-3xl">
                            <img src="/images/sidebiew.webp" alt="Happy in studio" width="200" height="auto"
                                loading="lazy" class="w-full h-full rd-2xl object-cover">
                        </div>
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