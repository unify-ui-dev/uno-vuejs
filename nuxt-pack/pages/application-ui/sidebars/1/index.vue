<script setup>
const sidebarIsToggled = useState('sidebarIsToggled',()=>false)
const sidebarIsResized = useState('sidebarIsResized',()=>false)


const toggleSidebar = () => {
    sidebarIsToggled.value = !sidebarIsToggled.value
    if (!sidebarIsToggled) {
        document.body.classList.toggle("overflow-y-auto")
    } else {
        document.body.classList.add("overflow-y-auto")
    }
}

const resizeSidebar = () => {
    sidebarIsResized.value = !sidebarIsResized.value
}

useHead({
    title: 'Sidebar',
    meta: [
        {
            name: 'description',
            content: 'Sidebar',
        },
    ],
    link: [
        {
            href: "https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap",
            rel: "stylesheet"
        }
    ]
})
</script>
<template>
    <aside un-bg="white dark:gray-950" shadow="lg gray-2/40 dark:gray-8/60"
        class="fixed h-[100dvh] overflow-hidden lg-static w11/12 max-w-[18rem] md-w72 transition-all rd-r-2xl flex flex-col justify-between px4 lg-transition-[width] ease-linear"
        :class="{
                '-translate-x-0': sidebarIsToggled,
                '-translate-x-full lg-translate-x-0': !sidebarIsToggled,
                '!lg-w20': sidebarIsResized,
                'lg-w72': !sidebarIsResized
            }">
        <div border-b="~ gray-2 dark:gray-8" class="min-h-max py4">
            <nuxt-link to="#" un-text="lg gray-8 dark:gray-2" class="flex items-center gap-x-3 font-semibold">
                <span class="w11 h11 min-w-[2.75rem] rd-md bg-blue-6 text-white flex items-center justify-center">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w6 h6">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M3 13.125C3 12.504 3.504 12 4.125 12h2.25c.621 0 1.125.504 1.125 1.125v6.75C7.5 20.496 6.996 21 6.375 21h-2.25A1.125 1.125 0 013 19.875v-6.75zM9.75 8.625c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125v11.25c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V8.625zM16.5 4.125c0-.621.504-1.125 1.125-1.125h2.25C20.496 3 21 3.504 21 4.125v15.75c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V4.125z" />
                    </svg>
                </span>
                <span :class="sidebarIsResized ? 'lg-op0 lg-invisible' : 'visible op100'">unifyUI</span>
            </nuxt-link>
        </div>
        <nav class="h-full pt-10">
            <ul text="gray-7 dark:gray-3" class="space-y-2">
                <li>
                    <nuxt-link to="#" un-text="gray-8 dark:white" bg="gray-2 dark:gray-8"
                        class="flex items-center gap-x-4 px3 py2.5 rd-md">
                        <span class="min-w-max inline-flex">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" class="w6 h6">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M6.429 9.75L2.25 12l4.179 2.25m0-4.5l5.571 3 5.571-3m-11.142 0L2.25 7.5 12 2.25l9.75 5.25-4.179 2.25m0 0L21.75 12l-4.179 2.25m0 0l4.179 2.25L12 21.75 2.25 16.5l4.179-2.25m11.142 0l-5.571 3-5.571-3" />
                            </svg>
                        </span>
                        <span class="inline-flex ease-linear transition-colors duration-300"
                            :class="sidebarIsResized ? 'lg-op0 lg-invisible' : 'op100 visible'">
                            Dashboard
                        </span>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="#" un-text="hover:gray-7 dark:hover:white" class="flex items-center gap-x-4 px3 py2.5">
                        <span class="min-w-max inline-flex">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" class="w6 h6">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M20.25 14.15v4.25c0 1.094-.787 2.036-1.872 2.18-2.087.277-4.216.42-6.378.42s-4.291-.143-6.378-.42c-1.085-.144-1.872-1.086-1.872-2.18v-4.25m16.5 0a2.18 2.18 0 00.75-1.661V8.706c0-1.081-.768-2.015-1.837-2.175a48.114 48.114 0 00-3.413-.387m4.5 8.006c-.194.165-.42.295-.673.38A23.978 23.978 0 0112 15.75c-2.648 0-5.195-.429-7.577-1.22a2.016 2.016 0 01-.673-.38m0 0A2.18 2.18 0 013 12.489V8.706c0-1.081.768-2.015 1.837-2.175a48.111 48.111 0 013.413-.387m7.5 0V5.25A2.25 2.25 0 0013.5 3h-3a2.25 2.25 0 00-2.25 2.25v.894m7.5 0a48.667 48.667 0 00-7.5 0M12 12.75h.008v.008H12v-.008z" />
                            </svg>
                        </span>
                        <span class="inline-flex ease-linear transition-colors duration-300"
                            :class="sidebarIsResized ? 'lg-op0 lg-invisible' : 'op100 visible'">
                            Candidats
                        </span>
                    </nuxt-link>
                </li>
            </ul>
        </nav>
        <div class="min-h-max py2 hidden lg-flex justify-end bg-transparent">
            <button @click="resizeSidebar" bg="gray-1 dark:gray-9" text="gray-8 dark:gray-2" border="~ gray-2 dark:gray-8"
                class="outline-none rd-md ease-linear transition-transform  w8 h8 sm-w9 sm-h9 flex items-center justify-center"
                :class="sidebarIsResized ? 'rotate-180' : ''" aria-label="resize sidebar">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w5 h5">
                    <path fill-rule="evenodd"
                        d="M12.79 5.23a.75.75 0 01-.02 1.06L8.832 10l3.938 3.71a.75.75 0 11-1.04 1.08l-4.5-4.25a.75.75 0 010-1.08l4.5-4.25a.75.75 0 011.06.02z"
                        clip-rule="evenodd" />
                </svg>
            </button>
        </div>
    </aside>
    <main>
        <div class="flex lg-hidden fixed right-2 top2 p4">
            <button @click="toggleSidebar" un-bg="blue-6 dark:blue-5"
                class="p3 rd-full outline-none w12 aspect-square flex flex-col relative justify-center items-center" aria-label="toggle sidebar">

                <span class="w6 h0.5 rd-full bg-gray-3 transition-transform duration-300 ease-linear"
                    :class="sidebarIsToggled ? 'translate-y-1.5 rotate-40' : ''"></span>
                <span class="w6 origin-center  mt-1 h-0.5 rd-full bg-gray-3 transition-all duration-300 ease-linear"
                    :class="sidebarIsToggled ? 'scale-x-0 op-0' : ''"></span>
                <span class="w6 mt1 h0.5 rd-full bg-gray-3 transition-all duration-300 ease-linear"
                    :class="sidebarIsToggled ? '-translate-y-1.5 -rotate-40' : ''"></span>
            </button>
        </div>
    </main>
</template>
<style >
body {
    --at-apply: font-inter bg-gray-1 dark-bg-gray-9
}
</style>