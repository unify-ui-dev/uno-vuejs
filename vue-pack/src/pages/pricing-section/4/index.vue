<script setup>
import { useHead } from 'unhead'


useHead({
    title: 'Pricing section',
    meta: [
        {
            name: 'description',
            content: 'My page description',
        },
    ],
    link: [
        {
            href: "https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&display=swap",
            rel: "stylesheet"
        }
    ]
})
</script>
<template>
    <section py32>
        <div max-w-7xl mx-auto px="5 sm:10 md:12 lg:5">
            <div flex flex-col space-y-16>
                <div flex gap-14 md-justify-between flex-col md-flex-row items-center>
                    <div text-="center md:left" md-max-w-lg space-y-5>
                        <span rd-lg bg="blue-1 dark:gray-9" px2.5 py1 font-semibold tracking-wide
                            text="xs blue-8 dark:gray-1">Plan</span>
                        <h2 font-semibold text="blue-950 dark:gray-2 3xl md:4xl xl:5xl" leading-tight>Choose perfet plan for
                            your need</h2>
                    </div>
                    <div min-w-max flex justify-center md-justify-end>
                        <div bg="white dark:gray-9" rd-xl shadow="lg gray-2/40 dark:none" flex items-center relative p1>
                            <button text-white flex items-center h9 w-max px4 rd-lg bg="blue-9 dark:blue-950">
                                Monthly
                            </button>
                            <button text="gray-7 dark:gray-3" flex items-center h9 w-max px4 bg-transparent>
                                Yearly
                            </button>
                        </div>
                    </div>
                </div>
                <div grid divide-y divide="gray-2 dark:gray-8" lg-divide-y-0 gap-6 mx-auto lg-items-stretch lg-grid-cols-3
                    gap="md:8 lg:12" bg="white dark:gray-9" rd-xl px="4 md:p6 lg:8" pb10>
                    <div bg="white dark:gray-9" pt6 px4 h-auto flex flex-col>
                        <div min-h-max mb5>
                            <div relative flex items-end>
                                <div class="flex">
                                    <span text="4xl blue-950 dark:white" font-bold>$0</span>
                                </div>
                                <span class="text-gray-7 dark:text-gray-3">/Month</span>
                            </div>
                            <h2 text="xl gray-8 dark:gray-2" font-semibold pt5>Educational</h2>
                            <p text="gray-7 dark:gray-3" pt-2>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                            </p>
                        </div>
                        <ul role="list" flex flex-col gap-2 text="gray-7 dark:gray-3">
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                        </ul>
                        <div mt5 flex flex-1 items-end min-h-max>
                            <a href="#" bg-transparent relative flex h12 w-full items-center justify-center px4
                                un-before="absolute content-empty inset-0 rd-lg bg-gray-9 dark:bg-gray-950 transition before:duration-3 active:scale-95 hover:bg-op-90">
                                <span relative text="sm white" font-medium>Continue for free</span>
                            </a>
                        </div>
                    </div>

                    <div bg="white dark:gray-9" pt6 px4 h-auto flex flex-col>
                        <div min-h-max mb5>
                            <div relative flex items-end>
                                <div flex>
                                    <span text="4xl blue-950 dark:white" font-bold>$20</span>
                                </div>
                                <span text="gray-7 dark:gray-3">/Month</span>
                            </div>
                            <h2 text="xl gray-8 dark:gray-2" font-semibold pt5>Team</h2>
                            <p text="gray-7 dark:gray-3" pt-2>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                            </p>
                        </div>
                        <ul role="list" flex flex-col gap-2 text="gray-7 dark:gray-3">
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                            <li flex gap-4 items-center>
                                <span bg="gray-1 dark:blue-950" text="sm gray-7 dark:gray-3" px2 py1 rd-full>&check;</span>
                                Advantage
                            </li>
                        </ul>
                        <div mt5 flex flex-1 items-end min-h-max>
                            <a href="#" bg-transparent relative flex h12 w-full items-center justify-center px4
                                un-before="absolute content-empty inset-0 rd-lg bg-gray-9 dark:bg-gray-950 transition before:duration-3 active:scale-95 hover:bg-op-90">
                                <span relative text="sm white" font-medium>Get started</span>
                            </a>
                        </div>
                    </div>

                    <div relative pt6 px4 mt6 lg:mt-0 h-auto flex flex-col
                        un-before="absolute content-empty z-0 scale-x-[1.13] before:scale-x-[1.15] lg:scale-x-105 scale-y-105 lg:scale-y-110 inset-0 bg-gray-9 dark:bg-blue-950 rd-xl">
                        <div class="absolute top-0 right-0 z-[5] bg-gray-5/40 dark:bg-blue-9 text-white rd-xl px-4 py-1">
                            Populaire</div>
                        <div class="min-h-max pb5 relative z-10">
                            <div relative flex items-end>
                                <div flex>
                                    <span text="4xl md:5xl white" font-bold>$0</span>
                                </div>
                                <span text="xl gray-2" font-semibold>/ Mois</span>
                            </div>
                            <h2 text="xl gray-1" font-semibold pt-5>Personnel</h2>
                            <p text-gray-3 pt2>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                            </p>
                        </div>
                        <ul role="list" flex flex-col h-full gap-2 text-gray-3 relative>
                            <li inline-flex gap-4 items-center>
                                <span bg="gray-5/40" text="sm gray-3" px2 py1 rd-full>&check;</span>
                                <span>Advantage 1</span>
                            </li>
                            <li inline-flex gap-4 items-center>
                                <span bg="gray-5/40" text="sm gray-3" px2 py1 rd-full>&check;</span>
                                <span>Advantage 1</span>
                            </li>
                            <li inline-flex gap-4 items-center>
                                <span bg="gray-5/40" text="sm gray-3" px2 py1 rd-full>&check;</span>
                                <span>Advantage 1</span>
                            </li>
                            <li inline-flex gap-4 items-center>
                                <span bg="gray-5/40" text="sm gray-3" px2 py1 rd-full>&check;</span>
                                <span>Advantage 1</span>
                            </li>
                            <li inline-flex gap-4 items-center>
                                <span bg="gray-5/40" text="sm gray-3" px2 py1 rd-full>&check;</span>
                                <span>Advantage 1</span>
                            </li>
                            <li inline-flex gap-4 items-center>
                                <span bg="gray-5/40" text="sm gray-3" px2 py1 rd-full>&check;</span>
                                <span>Advantage 1</span>
                            </li>
                        </ul>
                        <div mt5 flex min-h-max>
                            <a href="#" bg-transparent relative flex h12 w-full items-center justify-center px4
                                un-before="absolute content-empty inset-0 rd-lg bg-gray-2 dark:bg-gray-9 transition duration-3 hover:bg-op-90 active:duration-75 active:scale-95">
                                <span class="relative text-sm font-medium text-blue-9 dark:text-white">Continue for
                                    free</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style >
body {
    --at-apply: font-dms bg-gray-50 dark-bg-gray-950
}</style>