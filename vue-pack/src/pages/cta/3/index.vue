<script setup>
import { useHead } from 'unhead'


useHead({
  title: 'CTA',
  meta: [
    {
      name: 'description',
      content: 'Call to action',
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
    <section py24>
        <div px="5 sm:10 md:12 lg:5" class="max-w-5xl mx-auto text-center flex flex-col items-center space-y-8">
            <h1 text="4xl gray-9 dark:white" class="font-semibold">
                Start your free trial
            </h1>
            <p text="gray-7 dark:gray-3" class="max-w-md mx-auto">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor quaerat obcaecati dolore qui modi
            </p>
            <div class="flex gap-4 items-center">
                <a href="#" class="bg-blue-6 text-white px6 py3 rd-lg">
                    Get started
                </a>
                <a href="#" bg="gray-1 dark:gray-9" un-text="gray-8 dark:gray-2" border="~ gray-2 dark:gray-8" class="px6 py3 rd-lg">
                    Read doc
                </a>
            </div>
        </div>
    </section>
</template>
<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>