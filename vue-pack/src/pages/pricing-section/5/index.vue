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
  link:[
    {
        href:"https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&display=swap",
        rel:"stylesheet"
    }
  ]
})


</script>
<template>
    <main>
        <section py-32>
            <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto">
                <div class="flex flex-col space-y-12">
                    <div class="flex gap-10 flex-col items-center">
                        <div class="mx-auto max-w-3xl text-center space-y-8">
                            <span border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" text="gray-7 dark:gray-3" class="px3 py0.5 rd-full">
                                Pricing
                            </span>
                            <h1 text="3xl md:4xl xl:5xl gray-9 dark:white" class="font-bold">
                                Our pricing privacy
                            </h1>
                        </div>
                        <p text="gray-7 dark:gray-3 center" class="max-w-2xl mx-auto">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo illum voluptatibus optio quaerat
                        </p>
                    </div>
                    
                    <div class="grid gap-8 items-center sm-grid-cols-2 lg-grid-cols-3">
                        <div bg="white dark:gray-9" p="5 sm:6 md:8 xl:10" border="~ gray-3 dark:gray-8/80" class="md-hauto flex flex-col rd-3xl">
                            <span text="2xl gray-8 dark:gray-2" class="font-semibold">
                                Starter plan
                            </span>
                            <div text="2xl md:3xl gray-9 dark:white" class="mt2 font-bold">
                                450$
                            </div>
                            <p text="gray-7 dark:gray-3" class="mt-5 sm-mt-6">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo illum voluptatibus optio
                            </p>
                            <ul text="gray-6 dark:gray-4" class="flex flex-col space-y-3 mt5 sm-mt6">
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                            </ul>
                            <div class="mt-5 sm-mt-6">
                                <button bg="gray-8 hover:opacity-90" class="text-white transition-colors ease-leaner h12 rd-full px6
                                    w-full flex items-center gap-x-3 justify-center">
                                    Get started <span i-carbon-arrow-right flex> </span>
                                </button>
                            </div>
                        </div>
    
                        <div bg="gray-8 dark:gray-950" p="5 sm:6 md:8 xl:10" border="~ gray-8 dark:gray-9" class="rd-3xl flex flex-col">
                            <span class="font-semibold text-2xl text-gray-1">
                                Starter plan
                            </span>
                            <div text="white 2xl md:3xl" class="font-bold">
                                450$
                            </div>
                            <p class="mt-5 sm-mt-6 text-gray-2">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo illum voluptatibus optio
                            </p>
                            <ul class="flex flex-col space-y-3 mt5 sm-mt6 text-gray-3">
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>   
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>   
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>   
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>   
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>   
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>   
                                    </span>
                                    Included feature
                                </li>
                            </ul>
                            <div class="mt-5 sm-mt6">
                                <button class="bg-white hover-opacity-90 text-gray-9 transition-colors ease-leaner h12 rd-full px6
                                    w-full flex items-center gap-x-3 justify-center">
                                    Get started <span i-carbon-arrow-right flex></span>
                                </button>
                            </div>
                        </div>
    
                        <div bg="white dark:gray-9" p="5 sm:6 md:8 xl:10" border="~ gray-3 dark:gray-8/80" class="md-hauto flex flex-col rd-3xl">
                            <span text="2xl gray-8 dark:gray-2" class="font-semibold">
                                Starter plan
                            </span>
                            <div text="2xl md:3xl gray-9 dark:white" class="mt2 font-bold">
                                450$
                            </div>
                            <p text="gray-7 dark:gray-3" class="mt-5 sm-mt-6">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo illum voluptatibus optio
                            </p>
                            <ul text="gray-6 dark:gray-4" class="flex flex-col space-y-3 mt5 sm-mt6">
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                                <li class="flex items-center gap-x-3">
                                    <span text="blue-6 dark:blue-4">
                                        <span i-carbon-checkmark flex></span>                                          
                                    </span>
                                    Included feature
                                </li>
                            </ul>
                            <div class="mt-5 sm-mt-6">
                                <button bg="gray-8 hover:opacity-90" class="text-white transition-colors ease-leaner h12 rd-full px6
                                    w-full flex items-center gap-x-3 justify-center">
                                    Get started <span i-carbon-arrow-right flex> </span>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>
<style >
body{
    --at-apply: font-dms bg-gray-50 dark-bg-gray-950
}
</style>