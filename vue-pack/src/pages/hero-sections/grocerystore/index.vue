<script setup>
import { useHead } from 'unhead'
import { ref } from 'vue'

const navIsOpen = ref(false)
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

const features = [
    {
        id: 1,
        text: "Feature 1"
    },
    {
        id: 2,
        text: "Feature 2"
    },
    {
        id: 3,
        text: "Feature 3"
    },
    {
        id: 4,
        text: "Feature 4"
    },
]

const categories = [
    {
        id: 1,
        icon: "/images/icons/spinach-icon.svg",
        title: "Category 1",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
    {
        id: 2,
        icon: "/images/icons/green-grapes-icon.svg",
        title: "Category 2",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
    {
        id: 3,
        icon: "/images/icons/spinach-icon.svg",
        title: "Category 3",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
    {
        id: 4,
        icon: "/images/icons/spinach-icon.svg",
        title: "Category 4",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
    {
        id: 5,
        icon: "/images/icons/tomato-icon.svg",
        title: "Category 5",
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
]

</script>
<template>
    <div @click="closeNavBar()" aria-hidden="true" fixed bg="gray-8/40" class="inset-0 z30 hidden lg-hidden"
        :class="navIsOpen ? 'flex lg-hidden' : 'hidden'"></div>
    <header bg="emerald-50 dark:gray-950" fixed left-0 top-0 z40 w-full flex items-center h20
        border-b="~ gray-1 dark:gray-9">
        <nav relative mx-auto max-w-7xl w-full px="5 sm:10 md:12 lg:5" flex gap-x-5 justify-between items-center>
            <div flex items-center min-w-max>
                <router-link to="/" class="font-semibold text-xl text-gray8 dark-text-gray2">
                    <span relative un-text="emerald-8 dark:white"
                        un-after="absolute content-empty inset-0 rotate-3 border border-emerald-6">Grocy</span>Mart
                </router-link>
            </div>

            <div bg="white dark:gray-950 lg:transparent" border-b="~ gray-2 dark:gray-8 lg:none" py="8 lg:0"
                px="5 sm:10 md:12 lg:0" absolute left-0 top-full lg-top-0 w-full lg-relative lg-flex lg-justify-between
                duration-300 lg-transition-none ease-linear
                :class="navIsOpen ? 'translate-y-0 -rotate-0 op-100 visible' : 'translate-y-10 -rotate-12 op-0 invisible lg-visible lg-rotate-0 lg-translate-y-0 lg-op-100'">
                <ul
                    class="flex flex-col lg-flex-row gap-6 lg-items-center text-gray-8 dark-text-gray-2 lg-w-full lg-justify-center">
                    <li v-for="navItem in navItems" :key="navItem.id">
                        <router-link :to="navItem.href"
                            class="relative py2.5 duration-300 ease-linear hover-text-emerald-6 after-absolute after-content-empty after-w-full after-left-0 after-bottom-0 after-hpx after-rd-md after-origin-left after-ease-linear after-duration-300 after-scale-x-0 after-bg-emerald-6 hover-after-scale-100">
                            {{ navItem.text }}
                        </router-link>
                    </li>
                </ul>
                <div flex flex-col sm-flex-row sm-items-center gap-4 lg-min-w-max mt10 lg-mt-0>
                    <div class="hidden lg-flex lg-items-center">
                        <router-link to="#" class="relative px-1.5">
                            <span class="sr-only">cart</span>
                            <span absolute top-0 right-0 bg-emerald-6 w2 h2 rd-full></span>
                            <span i-carbon-shopping-cart bg="gray-7 dark:gray-3" flex text-2xl></span>
                        </router-link>
                    </div>
                    <router-link to="#"
                        class="px5 py2.5 rd-md text-emerald-8 dark-text-gray-2 underline flex justify-center">
                        Signin
                    </router-link>
                    <router-link to="#"
                        class="px5 py2.5 rd-md bg-emerald-6 hover-bg-emerald-7 text-white flex justify-center duration-300 ease-linear">
                        Signup
                    </router-link>
                </div>
            </div>
            <div flex items-center lg-hidden gap-x-4>
                <div class="flex items-center gap-x-4 lg-hidden">
                    <router-link to="#" class="px1.5 relative">
                        <span class="sr-only">cart</span>
                        <span absolute top-0 right-0 bg-emerald-6 w2 h2 rd-full></span>
                        <span i-carbon-shopping-cart bg="gray-7 dark:gray-3" class="flex text-2xl"></span>
                    </router-link>
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
    </header>

    <section py8 mt20>
        <div mx-auto max-w-7xl w-full px="5 sm:10 md:12 lg:5" flex flex-col lg-flex-row lg-items-center gap-x-6>
            <div py="4 lg:8 xl:12" space-y-7 w="lg:[47%]" max-w-2xl lg-max-w-none>
                <h1 text="gray-8 dark:white 3xl sm:4xl md:5xl xl:6xl" font-bold>
                    Let your <span text-emerald-6>groceries</span> come to you
                </h1>
                <p text="gray-7 dark:gray-3">
                    Get fresh groceries online without stepping out to make delicious food with the freshest ingredients
                </p>
                <div max-w-md w-full>
                    <form action="#" flex w-full un-text="gray-7 dark:gray-4">
                        <input type="text" placeholder="meal, Vegetables......" un-text="gray-9 dark:gray-2" px5 py2.5
                            border="~ emerald-2 dark:gray-8 r-0" rd-l-md flex w-full outline-none
                            bg="emerald-50 dark:gray-9">
                        <button aria-label="search button" outline-none text-white bg-emerald-6 px3 py2.5 rd-r-md min-w-max>
                            <span i-carbon-search text-xl flex></span>
                        </button>
                    </form>
                </div>
                <div grid grid-cols-2 gap-x-6 sm-gap-x-8 gap-y-4>
                    <div v-for="feature in features" :key="feature.id" class="text-gray-7 dark-text-gray-3 flex gap-x-3">
                        <span w7 h7 max-h-7 min-w="1.75rem" bg="emerald-1 dark:gray-8" text="emerald-6 dark:gray-3" rd-md
                            flex items-center justify-center>
                            &checkmark;
                        </span>
                        {{ feature.text }}
                    </div>
                </div>
            </div>
            <div flex flex-1 relative lg-h-auto>
                <div relative h-max flex justify-center w="11/12">
                    <span absolute top-0 left-32 w="3/5" aspect-square rd-md rotate="-30deg" translate-y-20 origin-center
                        border="~ emerald-2 dark:gray-8"></span>
                    <span absolute top="1/2" right-16 w="2/5" aspect-square rd-md rotate-12 translate-y="-1/2" origin-center
                        border="~ emerald-2 dark:gray-8"></span>
                    <img src="/images/woman-with-gro.webp" width="1001" height="1001" alt="woman with grocery" lg-w-full
                        relative>
                </div>
            </div>
        </div>
        <div mx-auto max-w-7xl bg="emerald-1 dark:gray-9" rd-md w-full p="5 sm:10 md:12 lg:5" grid grid-cols="2 sm:3 lg:5"
            gap-5>
            <div v-for="category in categories" :key="category.id" space-y-2 sm-p-4 sm-rd-md
                sm="bg-emerald-2/10 dark:bg-gray-8/10">
                <img :src="category.icon" :alt="category.title" width="96" height="96" w14 h14 md-w-20 md-h-20>
                <h2 font-semibold text="gray-8 dark:gray-2">
                    {{ category.title }}
                </h2>
                <p text="gray-7 dark:gray-3">
                    {{ category.description }}
                </p>
            </div>


        <div space-y-2 p4 rd-md bg="bg-emerald-2/10 dark:bg-gray-8/10" flex flex-col items-center justify-center
            border="emerald-1 dark:gray-7" lg-hidden>
            <button rd-full outline-none border="~ dashed emerald-3 dark:gray-7" p3>
                <span class="sr-only">Know more</span>
                <span i-carbon-add flex bg-emerald-6 text-xl></span>
            </button>
            <span class="text-gray-8 dark:text-gray-2">Know more</span>
        </div>
    </div>
</section></template>

<style >body {
    --at-apply: font-poppins bg-emerald-50 dark-bg-gray950
}</style>