<script setup>
const navIsOpen = useState('navIsOpen', () => false)
useHead({
    title: 'Grocery Store Herosection',
    meta: [
        {
            name: 'description',
            content: 'My page description',
        },
    ],
    link: [
        {
            href: "https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap",
            rel: "stylesheet"
        }
    ]
})

const navItems = [
    {
        id: 1,
        text: "Home",
        href: "/",
    },
    {
        id: 2,
        text: "Categories",
        href: "/",
    },
    {
        id: 3,
        text: "Sales",
        href: "/",
    },
    {
        id: 4,
        text: "About",
        href: "/",
    },
    {
        id: 5,
        text: "Contact",
        href: "/",
    }
]

function toggleNavBar() {
    navIsOpen.value = !navIsOpen.value
    document.body.classList.toggle("overflow-y-auto")
}
function closeNavBar() {
    navIsOpen.value = false
    ocument.body.classList.add("overflow-y-auto")
}
</script>
<template>
    <div @click="closeNavBar()" aria-hidden="true" fixed bg="gray-8/40" class="inset-0 z30 hidden lg-hidden"
        :class="navIsOpen ? 'flex lg-hidden' : 'hidden'"></div>
    <header bg="emerald-50 dark:gray-950" fixed left-0 top-0 z40 w-full flex items-center h20
        border-b="~ gray-1 dark:gray-9">
        <nav relative mx-auto max-w-7xl w-full px="5 sm:10 md:12 lg:5" flex gap-x-5 justify-between items-center>
            <div flex items-center min-w-max>
                <nuxt-link to="/" class="font-semibold text-xl text-gray8 dark-text-gray2">
                    <span relative un-text="emerald-8 dark:white"
                        un-after="absolute content-empty inset-0 rotate-3 border border-emerald-6">Grocy</span>Mart
                </nuxt-link>
            </div>

            <div bg="white dark:gray-950 lg:transparent" border-b="~ gray-2 dark:gray-8 lg:none" py="8 lg:0"
                px="5 sm:10 md:12 lg:0" absolute left-0 top-full lg-top-0 w-full lg-relative lg-flex lg-justify-between
                duration-300 lg-transition-none ease-linear
                :class="navIsOpen ? 'translate-y-0 -rotate-0 op-100 visible' : 'translate-y-10 -rotate-12 op-0 invisible lg-visible lg-rotate-0 lg-translate-y-0 lg-op-100'">
                <ul
                    class="flex flex-col lg-flex-row gap-6 lg-items-center text-gray-8 dark-text-gray-2 lg-w-full lg-justify-center">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <nuxt-link :to="navItem.href"
                            class="relative py2.5 duration-300 ease-linear hover-text-emerald-6 after-absolute after-content-empty after-w-full after-left-0 after-bottom-0 after-hpx after-rd-md after-origin-left after-ease-linear after-duration-300 after-scale-x-0 after-bg-emerald-6 hover-after-scale-100">
                            {{ navItem.text }}
                        </nuxt-link>
                    </li>
                </ul>
                <div flex flex-col sm-flex-row sm-items-center gap-4 lg-min-w-max mt10 lg-mt-0>
                    <div class="hidden lg-flex lg-items-center">
                        <nuxt-link to="#" class="relative px-1.5">
                            <span class="sr-only">cart</span>
                            <span absolute top-0 right-0 bg-emerald-6 w2 h2 rd-full></span>
                            <span i-carbon-shopping-cart bg="gray-7 dark:gray-3" flex text-2xl></span>
                        </nuxt-link>
                    </div>
                    <nuxt-link to="#" class="px5 py2.5 rd-md text-emerald-8 dark-text-gray-2 underline flex justify-center">
                        Signin
                    </nuxt-link>
                    <nuxt-link to="#"
                        class="px5 py2.5 rd-md bg-emerald-6 hover-bg-emerald-7 text-white flex justify-center duration-300 ease-linear">
                        Signup
                    </nuxt-link>
                </div>
            </div>
            <div flex items-center lg-hidden gap-x-4>
                <div class="flex items-center gap-x-4 lg-hidden">
                    <nuxt-link to="#" class="px1.5 relative">
                        <span class="sr-only">cart</span>
                        <span absolute top-0 right-0 bg-emerald-6 w2 h2 rd-full></span>
                        <span i-carbon-shopping-cart bg="gray-7 dark:gray-3" class="flex text-2xl"></span>
                    </nuxt-link>
                    <div class="flex">
                        <button @click="toggleNavBar()" aria-label="Toggle navbar" outline-none
                            border-l="~ emerald-1 dark:gray-7" pl3 relative py3 bg-transparent>
                            <div aria-hidden="true" bg="gray-8 dark:gray-2" h0.5 w6 rd transition duration-300
                                :class="navIsOpen ? 'rotate-45 translate-y-1.5' : ''"></div>
                            <div iaria-hidden="true" bg="gray-8 dark:gray-2" mt2 h0.5 w6 rd transition duration-300
                                :class="navIsOpen ? '-rotate-45 -translate-y-1.5' : ''"></div>
                        </button>
                    </div>
                </div>
            </div>
        </nav>
</header></template>

<style >body {
    --at-apply: font-poppins bg-emerald-50 dark-bg-gray950
}</style>