<script setup>
import { useHead } from 'unhead'

useHead({
  title: 'Footer sections',
  meta: [
    {
      name: 'description',
      content: 'Logo-cloud section',
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
    <footer class="pt2">
        <div px="2 sm:0">
            <div bg="gray-9 dark:blue-950" p="5 sm:10 y10 sm:y14 md:y16" class="mx-auto w-full max-w-6xl rd-3xl relative overflow-hidden">
                <div class="relative flex flex-col items-center text-center">
                    <h1 un-text="3xl sm:4xl md:5xl xl:6xl white" class="font-bold max-w-4xl"> Let's works on something togheter. </h1>
                    <p un-text="base gray-3" class="max-w-xl mt10"> Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequatur, nemo explicabo. Et, doloribus iusto. Inventore eligendi numquam, incidunt soluta nisi repudiandae asperiores </p>
                    <div class="flex justify-center mt10">
                        <router-link to="#" bg="white hover:gray-1/90" class="gap-x-3 font-display text-gray-9 px8 h12 rd-full flex items-center">
                            Let's talk
                            <span i-carbon-arrow-right flex text-2xl></span>                                                                    
                        </router-link>
                    </div>
                </div>
            </div>
        </div>
        <div bg="gray-2 dark:gray-9" class="pt60 -mt48 px4 sm-px10 md-px12 lg-px8">
            <div border-t="~ gray-3 dark:gray-7" class="w-full max-w-7xl mx-auto flex flex-col sm-flex-row sm-justify-between items-center gap-y-5 py3">
                <p text="gray-7 dark:gray-3">
                    &copy;  2023 unifyUi. Allrights reserved
                </p>
                <nav>
                    <ul text="gray-8 dark:gray-2" class="flex items-center gap-x-5">
                        <li>
                            <a href="#">
                                Term of services
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Portfolio
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Company
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </footer>
</template>
<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>