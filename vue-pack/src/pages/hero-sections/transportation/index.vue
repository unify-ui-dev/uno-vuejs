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
        text:"Agency",
        href:"#"
    },
    {
        id:2,
        text:"Services",
        href:"#"
    },
    {
        id:3,
        text:"Products",
        href:"#"
    },
    {
        id:4,
        text:"Services",
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
        class="sticky left-0 top-0 w-full flex items-center h20 z50 bg-white dark-bg-gray-950 bg-op-90 backdrop-filter backdrop-blur-xl">
        <nav px="5 sm:10 md:12 lg:5"
            class="relative mx-auto lg-max-w-7xl w-full flex gap-x-5 justify-between items-center">
            <div class="flex items-center min-w-max">
                <a href="#" class="font-semibold flex items-center gap-x-2">
                    <div class="flex items-center -space-x-3">
                        <span bg="blue-6 dark:blue-5" class="h6 aspect-square rd-full flex"></span>
                        <span bg="sky-6 dark:sky-4" class="h6 aspect-square blur rd-full flex"></span>
                    </div>
                    <span text="lg gray-7 dark:gray-3">careRent</span>
                </a>
            </div>

            <div data-navbar bg="white dark:gray-950 lg:!transparent" border-b="~ gray-2 dark:gray-8 lg:0" py="16 lg:0" px="5 sm:10 md:12 lg:0"
                class="absolute inset-0 top-0 h-screen lg-h-max left-0 lg-w-max lg-space-x-16 lg-top-0 lg-relative  lg-flex duration-300 ease-linear"
                :class="navIsOpen ? 'translate-y-0 op100 visible':'translate-y-10 op-0 invisible lg-visible  lg-translate-y-0 lg-op-100'">
                <ul text="gray-7 dark:gray-3"
                    class="flex flex-col lg-flex-row gap-6 lg-items-center lg-w-full lg-justify-center">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <router-link :to="navItem.href" class="py2.5 duration-300 ease-linear hover-text-blue-6">
                            {{navItem.text}}
                        </router-link>
                    </li>
                    
                </ul>
                <div class="flex flex-col sm-flex-row sm-items-center gap-4  lg-min-w-max mt-10 lg-mt-0">
                    <router-link to="#" class="flex items-center justify-center w-full sm-w-auto h12 px6 rd-full bg-gray-1 dark-bg-gray-9 text-blue-6 dark-text-gray-3 border  border-gray-2 dark-border-gray-8">
                        Get It touch
                    </router-link>
                </div>
            </div>
            <div aria-hidden="true" class="flex items-center lg-hidden">
                <button @click="toggleNavBar()" aria-label="toggle nav" border-l="~ blue-1 dark:gray-8"
                    class="outline-none pl3 relative py3 bg-transparent">
                    <div aria-hidden="true" bg="gray-8 dark:gray-3"
                        class="h0.5 w6 rd transition duration-300" :class="navIsOpen ? 'rotate-45 translate-y-1.5' : ''">
                    </div>
                    <div aria-hidden="true" bg="gray-8 dark:gray-3"
                        class="mt2 h0.5 w6 rd transition duration-300" :class="navIsOpen ? '-rotate-45 -translate-y-1.5' : ''"></div>
                </button>
            </div>
        </nav>
    </header>

    <section class="md-pt4">
        <div px="sm:2 md:2 lg:1 xl:0" class="mx-auto lg-max-w-[82rem]">
            <div bg="gray-1 dark:gray-9" class="rd-3xl overflow-hidden flex flex-col-reverse md-flex-row items-center">
                <div
                    class="absolute z10 bottom-8 lg-bottom-0 left-0 md-relative min-w-max w-full md-w-auto md-justify-center flex flex-row md-flex-col items-center md:space-y-4 gap-x-6 px-4 sm-pl8 sm-pr0 py4 text-gray-6">
                    <button border="~ gray-3 dark:gray-7" bg="gray-2 dark:gray-8" text="gray-8 dark:gray-2" class="outline-none p1.5 rd-full">
                        <span class="sr-only">Prev</span>
                        <span i-carbon-chevron-left flex text-md></span>
                    </button>
                    <div
                        class="flex md-flex-col items-center md-space-y-4 gap-x-4 w-max max-w-max">
                        <span border="~ gray-2 dark:gray-8" bg="gray-2 dark:gray-8" un-before="absolute content-empty inset-1 rd-full bg-blue-6" class="relative w5 h5 rd-full"></span>
                        <span border="~ gray-2 dark:gray-8" bg="gray-2/90 dark:gray-8/90" un-before="absolute content-emptyinset-1 rd-full" class="relative w5 h5 rd-full"></span>
                    </div>
                    <button border="~ gray-3 dark:gray-7" bg="gray-2 dark:gray-8" text="gray-8 dark:gray-2" class="outline-none p1.5 rd-full">
                        <span class="sr-only">Next</span>
                        <span i-carbon-chevron-right flex text-md></span>
                    </button>
                </div>
                <div class="w-full">
                    <div px="4 sm:8 md:12 lg:14" py="24 sm:20 md:24 lg:28" class="relative flex items-center min-h-[calc(100dvh-5rem)] md-min-h-none md-h-auto w-full">
                        <div class="sm-w-3/5 max-w-xl md-max-w-2xl relative z10">
                          <div class="space-y-6 md-space-y-8 relative">
                            <h1 text="3xl sm:4xl md:5xl xl:6xl white md:gray-9 dark:white" font-bold >
                              Freight and Transportation <span class="font-sans italic">Solutions</span>
                            </h1>
                            <p text="gray-3 md:gray-7 dark:gray-3" class="max-w-lg">
                              Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut ab, quos qui perspiciatis quibusdam,
                            </p>
                            <div class="pt4">
                              <a href="#" class="px6 h12 flex items-center w-max rd-3xl bg-blue-6 text-white">
                                Get In Touch
                              </a>
                            </div>
                          </div>
                        </div>
                        <div class="absolute right-0 top-0 inset-y-0 w-full md-w-4/5 lg-w-3/5">
                          <div aria-hidden="true" class="absolute inset-0 bg-gray-8/40 dark:bg-gray-950/80 md-hidden">
                            <span class="w-full md-hidden bg-gradient-to-br from-gray-8 dark-from-gray-950 flex h-full"></span>
                          </div>
                          <div class="hidden md-flex absolute inset-0 bg-gradient-to-r from-gray-1 dark-from-gray-9">
                          </div>
                          <img src="/images/camion1.webp" alt="Transportation" class="h-full w-full object-cover md-rd-r-3xl">
                        </div>
                      </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray950
}
</style>