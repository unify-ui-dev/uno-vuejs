<script setup>
import { useHead } from 'unhead'


useHead({
  title: 'Blog section',
  meta: [
    {
      name: 'description',
      content: 'Blog section',
    },
  ],
  link:[
    {
        href:"https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&display=swap",
        rel:"stylesheet"
    }
  ]
})


</script>
<template>
    <section py20>
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto space-y-14">
            <div class="flex md-justify-between">
                <div text="center md:left" class="space-y-6 max-w-2xl mx-auto md-mx-0">
                    <div text="center md:left" class="md-max-w-lg space-y-5">
                        <span bg="blue-1 dark:gray-9" text="xs blue-8 dark:gray-1" class="rd-lg px2.5 py1 font-semibold tracking-wide">Blog</span>
                        <h2 text="3xl md:4xl xl:5xl blue-950 dark:gray-2" class="font-semibold leading-tight">From our latest Blog Post</h2>
                    </div>
                </div>
                <div class="">
                    <a href="#" border="~ gray-1 dark:gray-9" text="blue-6 dark:gray-3" class="px6 py3 flex items-center gap-x-3">
                        See More
                        <span i-carbon-chevron-right text-lg></span>                       
                    </a>
                </div>
            </div>
            <div class="grid grid-cols-1 sm-grid-cols-2 gap-8 lg-gap-12 rd-t-lg">
                <div bg="white dark:gray-950" border="~ gray-1 dark:gray-9 hover:gray-2 dark:hover:gray-8" class="h-full duration-300 ease-linear p0.5 flex flex-col group">
                    <img alt="banner image" class="w-full aspect-video object-cover relative" src="https://devolio-template.vercel.app/_next/image?url=%2Fimages%2Farticle1.webp&w=1920&q=75" width="1263" height="1291">
                    <div class="px4 lg-px6 py5 lg-py8">
                        <a un-text="gray-9 dark:white 2xl lg:3xl" class="font-semibold" href="#">How to create a Hotel booking web application</a>
                        <div class="flex flex-wrap gap-x-2 w-full gap-y-3 pt5">
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Tailwindcss</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">webdesign</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">ui ux design</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Figma</span>
                        </div>
                    </div>
                </div>
                <div bg="white dark:gray-950" border="~ gray-1 dark:gray-9 hover:gray-2 dark:hover:gray-8" class="h-full duration-300 ease-linear p0.5 flex flex-col group">
                    <img alt="banner image" class="w-full aspect-video object-cover relative" src="https://devolio-template.vercel.app/_next/image?url=%2Fimages%2Farticle1.webp&w=1920&q=75" width="1263" height="1291">
                    <div class="px4 lg-px6 py5 lg-py8">
                        <a un-text="gray-9 dark:white 2xl lg:3xl" class="font-semibold" href="#">How to create a Hotel booking web application</a>
                        <div class="flex flex-wrap gap-x-2 w-full gap-y-3 pt5">
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Tailwindcss</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">webdesign</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">ui ux design</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Figma</span>
                        </div>
                    </div>
                </div>
                <div bg="white dark:gray-950" border="~ gray-1 dark:gray-9 hover:gray-2 dark:hover:gray-8" class="h-full duration-300 ease-linear p0.5 flex flex-col group">
                    <img alt="banner image" class="w-full aspect-video object-cover relative" src="https://devolio-template.vercel.app/_next/image?url=%2Fimages%2Farticle1.webp&w=1920&q=75" width="1263" height="1291">
                    <div class="px4 lg-px6 py5 lg-py8">
                        <a un-text="gray-9 dark:white 2xl lg:3xl" class="font-semibold" href="#">How to create a Hotel booking web application</a>
                        <div class="flex flex-wrap gap-x-2 w-full gap-y-3 pt5">
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Tailwindcss</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">webdesign</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">ui ux design</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Figma</span>
                        </div>
                    </div>
                </div>
                <div bg="white dark:gray-950" border="~ gray-1 dark:gray-9 hover:gray-2 dark:hover:gray-8" class="h-full duration-300 ease-linear p0.5 flex flex-col group">
                    <img alt="banner image" class="w-full aspect-video object-cover relative" src="https://devolio-template.vercel.app/_next/image?url=%2Fimages%2Farticle1.webp&w=1920&q=75" width="1263" height="1291">
                    <div class="px4 lg-px6 py5 lg-py8">
                        <a un-text="gray-9 dark:white 2xl lg:3xl" class="font-semibold" href="#">How to create a Hotel booking web application</a>
                        <div class="flex flex-wrap gap-x-2 w-full gap-y-3 pt5">
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Tailwindcss</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">webdesign</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">ui ux design</span>
                            <span bg="gray-1 dark:gray-9" text="blue-6 dark:gray-2" class="px2">Figma</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>