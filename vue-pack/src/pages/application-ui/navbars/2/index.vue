<script setup>
import { useHead } from 'unhead'
import { ref } from 'vue'

const navIsOpen = ref(false)
useHead({
  title: 'Architec Website Herosection',
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
        text:"Home",
        href:"/",
    },
    {
        id:2,
        text:"Services",
        href:"/",
    },
    {
        id:3,
        text:"About",
        href:"/",
    },
    {
        id:4,
        text:"Work",
        href:"/",
    },
    {
        id:5,
        text:"Pricing",
        href:"/",
    },
]

function toggleNavBar(){
    navIsOpen.value = !navIsOpen.value
}
function closeNavBar(){
    navIsOpen.value = false
}

</script>
<template>
    <div aria-hidden="true" @click="closeNavBar()" class="fixed bg-gray-8/40 inset-0 z30" :class="navIsOpen ? 'visible flex lg-hidden lg-invisible':'invisible hidden'"></div>
    <div mx-auto max-w-7xl w-full px="5 sm:10 md:12 lg:5">
        <div class="w-full flex justify-between h14 items-center">
            <div  text="gray-7 dark:gray-300" class="hfull flex items-center gap-x-4">
                <a href="tel:" flex gap-1 items-center text-sm>
                    <span i-carbon-phone text-xl bg="gray-7 dark:gray-3"></span>
                    <span class="hidden sm-flex">+243 97 24 44 966</span>
                </a>
                <a href="mailto:" flex gap-1 items-center text-sm>
                    <span i-carbon-email bg="gray-7 dark:gray-3" text-xl></span>
                    <span class="hidden sm-flex">johndoe@info.com</span>
                </a>
            </div>
            <div text="gray-7 dark:gray-300" class="flex items-center gap-x-2.5 -mx-2">
                <a href="#facebook" border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" p1 rd-md>
                    <span class="sr-only">facebook</span>
                    <span i-carbon-logo-facebook bg="gray-7 dark:gray-300 hover:pink-700" flex text-2xl transition ease-linear></span>
                </a>

                <a href="#twitter" p1 border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" rd-md>
                    <span class="sr-only">Twitter</span>
                    <span i-carbon-logo-twitter bg="gray-7 dark:gray-300 hover:pink-700" flex text-2xl transition ease-linear></span>
                </a>

                <a href="#linkedin" p1 border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" rd-md>
                    <span class="sr-only">linkedin</span>
                    <span i-carbon-logo-linkedin bg="gray-7 dark:gray-300 hover:pink-700" flex text-2xl transition ease-linear></span>
                </a>

                <a href="#instagram" p1 border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" rd-md>
                    <span class="sr-only">instagram</span>
                    <span i-carbon-logo-instagram bg="gray-7 dark:gray-300 hover:pink-700" flex text-2xl transition ease-linear></span>
                </a>
            </div>
        </div>
    </div>
    <header border-b="~ gray-1 dark:gray-9" bg="white dark:gray-950 op-80" class="relative backdrop-filter backdrop-blur-xl z50">
        <nav px="5 sm:10 md:12 lg:5" class="sticky z40 left-0 top-0 w-full flex items-center h20  mx-auto max-w-7xl gap-x-5 justify-between">
            <div flex items-center min-w-max>
                <router-link to="/" text-xl font-semibold flex items-center gap-x-2>
                    <span flex>
                        <span w3 h6 rd-l-full flex bg-red-5></span>
                        <span w3 h6 rd-r-full flex bg-pink-7 mt2></span>
                    </span>
                    <span text="lg gray-7 dark:gray-300">Archix</span>
                </router-link>
            </div>

            <div bg="white dark:gray-950  lg:transparent" border-b="~ gray-2 dark:gray-8 lg:none" 
                py="8 lg:0" px="5 sm:10 md:12 lg:0"  lg="flex justify-between"
                fixed top-20 left-0 w-full lg-top-0 lg-relative  duration-300 ease-linear
                :class="navIsOpen ? 'visible op100 translate-y-0':'translate-y-10 lg-translate-y-0 invisible lg-visible op0 lg-op100'">
                <ul text="gray-7 dark:gray-300" flex flex-col lg-flex-row gap-6 lg-items-center lg-w-full lg-justify-center>
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <router-link :to="navItem.href"  class="py2.5 duration-300 ease-linear hover-text-pink-6"> 
                            {{ navItem.text }}
                        </router-link>
                    </li>
                </ul>
                <div flex sm-items-center lg-min-w-max mt-10 lg-mt-0>
                    <router-link to="#" class="px-6 items-center h-12 rd-3xl text-pink-7 dark-text-white border border-gray-2 dark-border-gray-8 bg-gray-1 dark-bg-gray-9 duration-300 ease-linear flex justify-center w-full sm-w-auto">
                        Book a call
                    </router-link>
                </div>
            </div>
            <div aria-hidden="true" class="flex items-center lg:hidden">
                <button @click="toggleNavBar()" aria-label="toggle navbar" border-l="~ gray-1 dark:gray-9" class="outline-none bg-transparent pl3 relative py3">
                    <div h0.5 w6 rd bg="gray-7 dark:gray-3" transition duration-300 aria-hidden="true" :class="navIsOpen ? 'rotate-45 translate-y-1.5':''">
                    </div>
                    <div mt2 h0.5 w6 rd bg="gray-7 dark:gray-3" transition duration-300 aria-hidden="true" :class="navIsOpen ? '-rotate-45 -translate-y-1.5':''">
                    </div>
                </button>
            </div>
        </nav>
    </header>
</template>

<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray950
}
</style>