<script setup>
const navIsOpen = useState('navIsOpen', ()=>false)
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
        text:"Features",
        href:"#"
    },
    {
        id:2,
        text:"Company",
        href:"#"
    },
    {
        id:3,
        text:"Plateform",
        href:"#"
    },
    {
        id:4,
        text:"Resources",
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
                <nuxt-link to="#" class="font-semibold flex items-center gap-x-2">
                    <div class="flex items-center -space-x-3">
                        <span bg="purple-6 dark:purple-5" class="h6 aspect-square rd-full flex"></span>
                        <span bg="pink-6 dark:pink-4" class="h6 aspect-square blur rd-full flex"></span>
                    </div>
                    <span text="lg text-gray-7 dark:gray-3">mySto</span>
                </nuxt-link>
            </div>

            <div bg="white dark:gray-950 lg:!transparent" py="32 lg:0" px="5 sm:10 md:12 lg:0"
                class="fixed inset-x-0 h-[100dvh] lg-h-max top-0 left-0 w-full lg-top-0 lg-relative  lg-flex lg-justify-between duration-300 ease-linear"
                :class="navIsOpen ? 'translate-y-0 op100 visible':' -translate-y-10 op-0 invisible lg-visible  lg-translate-y-0 lg-op-100'">
                <ul text="gray-7 dark:gray-3"
                    class="flex flex-col lg-flex-row gap-6 lg-items-center lg-w-full lg-pl-10">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <nuxt-link :to="navItem.href" class="py2.5 duration-300 ease-linear hover:text-purple-6">
                            {{navItem.text}}
                        </nuxt-link>
                    </li>
                </ul>
                <div
                    class="flex flex-col sm-flex-row sm-items-center gap-4  lg-min-w-max mt-10 lg-mt-0">
                    <nuxt-link to="#" class="h10 flex items-center justify-center w-full sm-w-max rd-full px5 border border-gray-2 dark-border-gray-8 text-purple-6 dark-text-gray-3">
                        Login
                    </nuxt-link>
                    <nuxt-link to="#" class="h10 flex items-center justify-center w-full sm-w-max rd-full px5 bg-purple-6 text-white border border-transparent">
                        Sign-up
                    </nuxt-link>
                </div>
            </div>
            <div class="flex items-center lg-hidden">
                <button @click="toggleNavBar()" aria-label="toggle navbar" border-l="~ purple-1 dark:gray-8"
                    class="focus-outline-none pl-3 relative py3 bg-transparent">
                    <div aria-hidden="true" bg="gray-8 dark:gray-3"
                        class="h0.5 w6 rd transition duration-300" :class="navIsOpen?'rotate-45 translate-y-1.5':''">
                    </div>
                    <div aria-hidden="true" bg="gray-8 dark:gray-3"
                        class="mt2 h0.5 w6 rd transition duration-300" :class="navIsOpen?'-rotate-45 -translate-y-1.5':''"></div>
                </button>
            </div>
        </nav>
    </header>

    <section class="min-h-max bg-purple-50 dark-bg-gray-950">
        <div class="absolute top-0 inset-x-0 h40 bg-gradient-to-br from-purple-3 op-90 blur-lg dark-from-purple-8 dark-blur-xl dark-op-40"></div>
        <div class="w-full flex items-center relative">
            <div class="absolute top-1/2 left-1/2 -translate-y-1/2 -translate-x-1/2 w-2/5 aspect-[2/0.5] bg-gradient-to-br from-purple-6 to-pink-4 rd-full op-50 blur-2xl"></div>
            <div px="5 sm:10 md:12 lg:5" class="min-h-max relative mx-auto pt32 lg-max-w-7xl w-full text-center space-y-10">
                <nuxt-link to="#" class="flex items-center gap-x-2 mx-auto w-max px2 pr1 py1 rd-full text-gray-9 dark-text-gray-1 bg-gray-1 dark-bg-gray-9 border border-gray-3 dark-border-gray-8">
                    mySto v2.1 is out
                    <span bg="gray-2 dark:gray-8" class="px1 rd-full">
                        <span i-carbon-arrow-right text-lg flex></span>                          
                    </span>
                </nuxt-link>
                <h1 text="gray-9 dark:white 4xl/tight sm:5xl/tight lg:6xl/tight" class="mx-auto max-w-5xl font-semibold">
                    The Tool that lets you have full control on your stock & sales
                </h1>
                <p text="gray-7 dark:gray-3" class="mx-auto max-w-2xl">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt saepe atque enim quasi a ipsum asperiores necessitatibus deleniti, sint quo vel corporis dignissimos
                </p>
                <div class="flex sm-flex-row flex-col gap-5 w-full mx-auto max-w-lg">
                    <form action="#" text="gray-6 dark:gray-4" bg="gray-1 dark:gray-9 focus-within:white dark:focus-within:gray-950" border="~ gray-2 dark:gray-8  focus-within:puble-6" shadow="lg gray-2/20 dark:transparent"
                        class="py1 pl6 w-full pr1 flex gap-3 items-center
                            rd-full ease-linear">
                        <input type="email" name="" id="" placeholder="johndoe@gmail.com"
                            class="w-full py3 focus-outline-none bg-transparent">
                        <button aria-label="sign up"
                            after="absolute content-empty inset-x-0 aspect-square scale-0 op-70 origin-center duration-300 ease-linear top-0 left-0 bg-purple-7 hover:op-100 hover:scale-[2.5]" 
                            class="flex text-white justify-center items-center w-max min-w-max sm:w-max px-6 h-12 rd-full focus-outline-none relative overflow-hidden border duration-300 ease-linear
                                 bg-purple-6 border-transparent hover-border-[#172554]">
                            <span class="hidden sm:flex relative z-[5]">
                                Sign up
                            </span>
                            <span class="flex sm-hidden relative z-[5]">
                                <span i-carbon-send text-xl></span>
                            </span>
                        </button>
                    </form>
                </div>
                <div  class="mx-auto max-w-6xl rd-t-2xl aspect-[5/2.3] overflow-hidden bg-gradient-to-t from-gray-50 to-gray-2 dark-from-gray-950 dark-to-gray-9 px2 pt2">
                    <img src="/images/dash-light.webp" width="1440" height="1024" alt="product image" class="rd-2xl w-full h-auto dark-hidden">
                    <img src="/images/dash-dark.webp" width="1440" height="1024" alt="product image" class="rd-2xl w-full h-auto hidden dark-flex">
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