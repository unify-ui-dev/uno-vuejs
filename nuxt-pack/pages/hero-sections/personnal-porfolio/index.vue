<script setup>
const navIsOpen = useState('navIsOpen', ()=>false)
useHead({
  title: 'Personnal Website Herosection',
  meta: [
    {
      name: 'description',
      content: 'My page description',
    },
  ],
  link:[
    {
        href:"https://fonts.googleapis.com/css2?family=Oswald:wght@400;600&family=Poppins:wght@300;400;500;600;700&display=swap",
        rel:"stylesheet"
    }
  ]
})

const navItems = [
    {
        id:1,
        text:"Home",
        isActive:true,
        href:"#"
    },
    {
        id:2,
        text:"Portfolio",
        isActive:false,
        href:"#"
    },
    {
        id:3,
        text:"Blog",
        isActive:false,
        href:"#"
    },
    {
        id:4,
        text:"About",
        isActive:false,
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
    <header sticky left-0 top-0 w-full flex items-center h20 bg="white dark:gray-950" 
        border-b="~ gray-2 dark:gray-7" z40>
        <nav relative mx-auto max-w-7xl w-full px="5 sm:10 md:12 lg:5" flex gap-x-5 justify-between items-center>
            <div aria-hidden="true" class="w-full flex items-center lg-hidden">
                <button @click="toggleNavBar()" aria-label="toggle navbar" border-r="~ gray-2 dark:gray-8" outline-none bg-transparent relative py3 pr3>
                    <div aria-hidden="true" h0.5 w6 rd  transition duration-300 bg="gray-8 dark:gray-2" :class="navIsOpen ? 'rotate-45 translate-y-1.5' : ''"></div>
                    <div aria-hidden="true" mt2 h0.5 w6 rd transition duration-300 bg="gray-8 dark:gray-2" :class="navIsOpen ? '-rotate-45 -translate-y-1.5' : ''"></div>
                </button>
            </div>
            <div absolute lg-relative lg-flex w-full top-full lg-top-0 left-0 bg="white  dark:gray-950 lg:transparent dark:lg:transparent"  border-b="~ gray-2 dark:gray-8 lg:0" ease-linear duration-300 
            :class="navIsOpen ? 'visible op100' : 'invisible op0 lg-visible lg-op-100'">
                <ul px="5 sm:10 md:12 lg:0" flex flex-col lg:flex-row lg:items-center  py="4 lg:0" gap="y-6 lg:x-5" text="gray-7 dark:gray-3">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <nuxt-link v-if="navItem.isActive" :to="navItem.href" class="relative py3 after-absolute after-content-empty after-bottom-0 after-left-0 after-h0.5 after-rd-lg after-bg-gray-6 after-w4">
                            {{navItem.text}}
                        </nuxt-link>
                        <nuxt-link v-else="navItem.hasDropDown" :to="navItem.href" class="relative py3 after-absolute before-content-empty before-bottom-0 before-left-0 before-h0.5 before-rd-lg before-bg-transparent before-w4">
                            {{navItem.text}}
                        </nuxt-link>
                    </li> 
                </ul>
            </div>
            <div class="flex items-center flex-1">
                <nuxt-link to="/" class="text-gray-8 dark-text-gray-2 flex items-center gap-x-0.5">
                    <span bg="gray-7 dark:gray-8" text-white px4 py1.5 rd-lg>R</span>
                    <span aria-hidden="true" class="hidden sm-flex">doe</span>
                </nuxt-link>
            </div>
            <div flex justify-end items-center gap-x="1.5 sm:2" w-full text="gray-7 dark:gray-3">
                <nuxt-link to="#" target="_blank" duration-200 ease-linear hover="text-gray-8 dark:text-gray-2">
                    <span class="sr-only">facebook</span>
                    <span i-carbon-logo-facebook flex p3 sm-p3.5 bg="gray-8 dark:gray-2"></span>
                </nuxt-link>
                <nuxt-link to="#" target="_blank" duration-200 ease-linear hover="text-gray-8 dark:text-gray-2">
                    <span class="sr-only">Instagram</span>
                    <span i-carbon-logo-instagram flex p3 sm-p3.5 bg="gray-8 dark:gray-2"></span>
                </nuxt-link>
                <nuxt-link to="#" target="_blank" duration-200 ease-linear hover="text-gray-8 dark:text-gray-2">
                    <span class="sr-only">Twitter</span>
                    <span i-carbon-logo-twitter flex p3 sm-p3.5 bg="gray-8 dark:gray-2"></span>
                </nuxt-link>
                <nuxt-link to="#" target="_blank" duration-200 ease-linear hover="text-gray-8 dark:text-gray-2">
                    <span class="sr-only">github</span>
                    <span i-carbon-logo-github flex p3 sm-p3.5 bg="gray-8 dark:gray-2"></span>
                </nuxt-link>
            </div>
        </nav>
    </header>

    <section py-8>
        <div px="5 sm:10 md:12 lg:5" class="mx-auto max-w-7xl w-full">
            <div class="mx-auto text-center max-w-xl">
                <h1 class="font-semibold  relative max-w-max mx-auto pb-2 text-3xl sm-text-4xl md-text-5xl text-gray-7 dark:text-white"
                    un-after="absolute content-empty bottom-0 left-0 h0.5 rd-lg bg-gray-7 dark:bg-gray-1 w4">
                    Roy Doe doe
                </h1>
            </div>
            <div class="mt8 grid md-grid-cols-2 lg-grid-cols-3 gap-x-6 lg-gap-x-14 gap-y-8 md-items-end">
                <div space-y="4 md:6" col-span="md:2 lg:1" text="center lg:left" w-full max-w-3xl lg-max-w-none mx-auto>
                    <h1 text="2xl md:3xl gray-8 dark:white" font-semibold>
                        Web designer based in Lubumbashi-DRC
                    </h1>
                    <div text="gray-7 dark:gray-3" mx-auto max-w-2xl lg-max-w-none space-y-3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
                            labore et dolore magna aliqua. </p>
                        <p>
                            Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
                        </p>
                    </div>
                    <div class="flex justify-center lg-justify-start">
                        <nuxt-link to="#" class="bg-gray-9 dark-bg-white hover-bg-opacity-90 text-white dark-text-gray-9 text-sm px6 h11 flex items-center rd-lg transition ease-linear">
                            Hire me
                        </nuxt-link>
                    </div>
                    <div class="grid grid-cols-3 w-full">
                        <div>
                            <h2 text="xl md:2xl gray-8 dark:gray-2" font-semibold>
                                2years</h2>
                            <span text="gray-6 dark:gray-3">Experience</span>
                        </div>
                        <div>
                            <h2 text="xl md:2xl gray-8 dark:gray-2" font-semibold>
                                +10</h2>
                            <span text="gray-6 dark:gray-3">Projects</span>
                        </div>
                        <div>
                            <h2 text="xl md:2xl gray-8 dark:gray-2" font-semibold>
                                90%</h2>
                            <span text="gray-6 dark:gray-3">Satisfaction</span>
                        </div>
                    </div>
                </div>
                <div flex justify-center>
                    <div class="max-w-full relative">
                        <span
                            class="absolute inset-x-0 top-16 bottom-0 rd-lg scale-[1.04]  bg-gradient-to-b from-gray-2 dark-from-gray-8"></span>
                        <span class="absolute inset-x-0 bottom-0 top-16 rd-lg bg-gray-1 dark:bg-gray-9"></span>
                        <img src="/images/dev-with-c.webp" width="1240" height="1376" alt="Developer with laptop smile"
                            class="relative w-full h-auto max-h-96 lg-max-h-[26rem]">
                    </div>
                </div>
                <div class="space-y-3 lg-space-y-6">
                    <div p="2 md:3 lg:4" bg="gray-50 dark:gray-9" border="~ gray-1/80 dark:gray-9/80" flex items-start gap-x-4  rd-lg>
                        <span min-w-max text="gray-6 dark:gray-2" p-2 md:p-3 rd-lg bg="gray-2 dark:gray-8" border="~ gray-1/70 dark:gray-9/7">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" width="24" height="24" class="w6 h6">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M3.75 13.5l10.5-11.25L12 10.5h8.25L9.75 21.75 12 13.5H3.75z" />
                            </svg>
                        </span>
                        <div>
                            <span font-semibold text="gray-8 dark:gray-2 lg">Smart Skills</span>
                            <p text="gray-7 dark:gray-3">
                                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                            </p>
                        </div>
                    </div>
                    <div p="2 md:3 lg:4" bg="gray-50 dark:gray-9" border="~ gray-1/80 dark:gray-9/80" flex items-start gap-x-4  rd-lg>
                        <span min-w-max text="gray-6 dark:gray-2" p-2 md:p-3 rd-lg bg="gray-2 dark:gray-8" border="1 gray-1/70 dark:gray-9/7">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" width="24" height="24" class="w6 h6">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M14.25 6.087c0-.355.186-.676.401-.959.221-.29.349-.634.349-1.003 0-1.036-1.007-1.875-2.25-1.875s-2.25.84-2.25 1.875c0 .369.128.713.349 1.003.215.283.401.604.401.959v0a.64.64 0 01-.657.643 48.39 48.39 0 01-4.163-.3c.186 1.613.293 3.25.315 4.907a.656.656 0 01-.658.663v0c-.355 0-.676-.186-.959-.401a1.647 1.647 0 00-1.003-.349c-1.036 0-1.875 1.007-1.875 2.25s.84 2.25 1.875 2.25c.369 0 .713-.128 1.003-.349.283-.215.604-.401.959-.401v0c.31 0 .555.26.532.57a48.039 48.039 0 01-.642 5.056c1.518.19 3.058.309 4.616.354a.64.64 0 00.657-.643v0c0-.355-.186-.676-.401-.959a1.647 1.647 0 01-.349-1.003c0-1.035 1.008-1.875 2.25-1.875 1.243 0 2.25.84 2.25 1.875 0 .369-.128.713-.349 1.003-.215.283-.4.604-.4.959v0c0 .333.277.599.61.58a48.1 48.1 0 005.427-.63 48.05 48.05 0 00.582-4.717.532.532 0 00-.533-.57v0c-.355 0-.676.186-.959.401-.29.221-.634.349-1.003.349-1.035 0-1.875-1.007-1.875-2.25s.84-2.25 1.875-2.25c.37 0 .713.128 1.003.349.283.215.604.401.96.401v0a.656.656 0 00.658-.663 48.422 48.422 0 00-.37-5.36c-1.886.342-3.81.574-5.766.689a.578.578 0 01-.61-.58v0z" />
                            </svg>
                        </span>
                        <div>
                            <span font-semibold text="gray-8 dark:gray-2 lg">Smart Skills</span>
                            <p text="gray-7 dark:gray-3">
                                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                            </p>
                        </div>
                    </div>
                    <div p="2 md:3 lg:4" bg="gray-50 dark:gray-9" border="~ gray-1/80 dark:gray-9/80" flex items-start gap-x-4  rd-lg>
                        <span min-w-max text="gray-6 dark:gray-2" p-2 md:p-3 rd-lg bg="gray-2 dark:gray-8" border="1 gray-1/70 dark:gray-9/7">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" width="24" height="24" class="w6 h6">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M3.75 13.5l10.5-11.25L12 10.5h8.25L9.75 21.75 12 13.5H3.75z" />
                            </svg>
                        </span>
                        <div>
                            <span font-semibold text="gray-8 dark:gray-2 lg">Smart Skills</span>
                            <p text="gray-7 dark:gray-3">
                                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                            </p>
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