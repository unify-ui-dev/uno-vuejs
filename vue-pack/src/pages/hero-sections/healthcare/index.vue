<script setup>
import { useHead } from 'unhead'
import { ref } from 'vue'

const navIsOpen = ref(false)
useHead({
  title: 'Healthcare Herosection',
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
        text:"Blog",
        href:"/",
    },
    {
        id:5,
        text:"FAQ",
        href:"/",
    }
]

function toggleNavBar(){
    navIsOpen.value = !navIsOpen.value
    document.body.classList.toggle("overflow-y-auto")
}
function closeNavBar(){
    navIsOpen.value = false
    ocument.body.classList.add("overflow-y-auto")
}

const stats = [
    {
        id:1,
        stat:450,
        title:"Diagnostic Weekly"
    },
    {
        id:2,
        stat:368,
        title:"Patients"
    },
    {
        id:3,
        stat:"20k",
        title:"Diagnostic Weekly"
    },
]

</script>
<template>
    <div @click="closeNavBar()" daria-hidden="true" class="fixed bg-gray-8/40 inset-0 z-30" :class="navIsOpen ? 'flex lg-hidden' : 'hidden'"></div>
    <header absolute inset-x-0 top-0 flex items-center h20 z40>
        <nav relative mx-auto max-w-7xl w-full px="5 sm:10 md:12 lg:5" flex gap-x-5 justify-between items-center>
            <div flex items-center min-w-max>
                <router-link to="#" class="text-xl text-gray-8 dark-text-gray-2 font-semibold">
                    <span relative un-after="absolute content-empty inset-0 rotate-3 border border-blue-6"
                        text="blue-6 dark:blue-4">Health</span>Care
                </router-link>
            </div>

            <div bg="white dark:gray-950 lg:!transparent"
                border-b="~ gray-2 dark:gray-8 lg:none" py="8 lg:0" px="5 sm:10 md:12 lg:0"
                absolute top-full lg-relative lg-top-0 left-0 w-full lg-w-max lg-flex duration-300 ease-linear gap-x-6
                :class="navIsOpen ? 'translate-y-0 op-100 visible' : 'translate-y-10 op-0 invisible lg-visible lg-translate-y-0 lg-op-100'"
                >
                <ul flex flex-col gap-6 text="gray-7 dark:gray-3"
                    lg="justify-center flex-row w-full items-center">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <router-link :to="navItem.href"  class="duration-300 ease-linear hover-text-blue-6">
                            {{navItem.text}}
                        </router-link>
                    </li>
                </ul>
                <div flex flex-col sm-flex-row sm-items-center gap-4 lg-min-w-max mt="10 lg:0">
                    <router-link to="#" class="relative px6 py3 flex justify-center items-center text-white rd-3xl transition
                        ease-linear bg-blue-6 hover-bg-blue-8 focus-bg-blue-7">
                        <span relative>
                            Get in touch
                        </span>
                    </router-link>
                </div>
            </div>
            <div flex items-center lg-hidden>
                <button @click="toggleNavBar()" aria-label="toggle navabar" outline-none border-l="~ gray-3 dark:gray-5" pl3
                    relative py3 bg-transparent>
                    <div id="line-1" aria-hidden="true" h0.5 w6 rd bg-gray-7 dark-bg-gray-3 transition duration-300 :class="navIsOpen ? 'rotate-45 translate-y-1.5' : ''">
                    </div>
                    <div id="line-2" aria-hidden="true" mt2 h0.5 w6 rd bg-gray-7 dark-bg-gray-3 transition
                        duration-300 :class="navIsOpen ? '-rotate-45 -translate-y-1.5' : ''"></div>
                </button>
            </div>
        </nav>
    </header>

    <main>
        <section relative bg="blue-50 dark:gray-900" pb20 pt="26 lg:24">
            <div class="absolute top-0 inset-x-0 h64 flex items-start">
                <div
                    class="h24 w2/3 bg-gradient-to-br from-blue-500 op20 blur-2xl dark-from-[#0c1cac] dark-invisible dark-op-40">
                </div>
                <div
                    class="h20 w-3/5 bg-gradient-to-r from-[#488ad4] op40 blur-2xl dark-from-[#0c1cac] dark-op-40">
                </div>
            </div>
            <div px="5 sm:10 md:12 lg:5" relative mx-auto max-w-7xl w-full flex flex-col lg-flex-row
                gap="8 lg:10 xl:12">

                <div aria-hidden="true" absolute inset-y-0 w44 left-0 hidden dark-flex>
                    <div
                        class="h-full md-h-1/2 lg-h-full w-full bg-gradient-to-tr op40 dark-blur-2xl dark-from-[#0c1cac] dark-op-20">
                    </div>
                </div>

                <div mx-auto space-y-8 text-center flex flex-col max-w-2xl justify-center flex-1
                    lg="flex justify-start py-8 w-1/2 max-w-none text-left">
                    <h1 text="blue-950 dark:white 3xl/snug sm:5xl/tight lg:4xl/tight xl:[3.50rem]/tight" font-bold>
                        We are providing best and affordable health care.
                    </h1>
                    <p text="gray-7 dark:gray-3 lg:lg" max-w-2xl lg-max-w-none mx-auto>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos, fugit! Laborum quo maxime
                        at sapiente
                        quasi
                    </p>
                    <form action="#" flex max-w="34rem" lg-max-w-none mx="auto lg:0" w-full relative
                        bg="gray-1 dark:gray-950/60" border="~ blue-1 dark:gray-950/60" overflow-hidden p0.5 rd-3xl
                        un-before="absolute content-empty inset-1 bg-blue-50 dark:bg-gray-950 rd-[1.25rem]">
                        <input type="text" placeholder="johndoe@gmail.com"
                            class="peer relative w-full bg-white dark-bg-gray-950 px5 py3 rd-full outline-none text-gray-6 dark-text-gray-3">
                        <button
                            class="absolute inset-y-1.5 right-1.5 bg-blue-6 text-white p3 sm-px-6 flex items-center rd-full bg-blue-6 hover-bg-blue-8 focus-bg-blue-7">
                            <span class="hidden sm-flex relative z5">Get in touch</span>
                            <span flex sm-hidden relative z5>
                                <span i-carbon-send text-2xl bg-white></span>
                            </span>
                        </button>
                    </form>
                    <div grid grid-cols="2 md:3" gap-4 max-w="[34rem]" mx-auto lg-mx-0 w-full>
                        <div v-for="stat_ in stats" :key="stat_.id" relative text-center bg="white dark:gray-950/60" border="~ blue-1 dark:gray-950" p5 rd-3xl
                            un-before="absolute content-empty inset-1 bg-blue-50 dark:bg-gray-950 rd-[1.25rem]">
                            <span font-bold text="2xl gray-8 dark:gray-1" relative>
                                {{ stat_.stat }}
                            </span>
                            <h2 text="sm gray-7 dark:gray-3" relative>{{ stat_.title }}</h2>
                        </div>
                    </div>
                </div>
                <div class="hidden md-flex flex-1 justify-center  lg-w-1/2 relative w-full max-w-3xl lg-max-w-none mx-auto">
                    <div md="w-5/6 h-auto" lg="w-full h-full absolute right-0" bg-blue-1 overflow-hidden rounded-b="24px">
                        <img src="/images/medecine-team.webp" alt="happy team" width="1850" height="auto"
                            class="w-full h-full object-cover">
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray950
}
</style>