<script setup>
import { useHead } from 'unhead'


useHead({
  title: 'Content section',
  meta: [
    {
      name: 'description',
      content: 'COntent section',
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
    <section class="py24">
        <div class="max-w-7xl mx-auto px-5 sm-px10 md-px12 lg-px5 flex flex-col md-flex-row gap-16">
            <div class="md-w-1/2 space-y-12 text-gray7 dark-text-gray3">
                <h1 class="text-gray9 dark-text-white font-semibold text-2xl sm-text-3xl md-text-4xl">
                    We help drive your business forward faster
                </h1>
                <p>
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minus, saepe aliquid autem alias vero distinctio dignissimos consequatur? Excepturi quibusdam, quam ipsum hic, laudantium ducimus suscipit, culpa facere consequuntur repellat delectus.
                </p>
                <ul class="space-y4">
                    <li class="flex items-center gap-x-4">
                        <span class="w5 h5 text-sm flex items-center justify-center rd-full bg-emerald-7 dark-bg-emerald-6 text-white">&check;</span>
                        Web site Analysis
                    </li>
                    <li class="flex items-center gap-x-4">
                        <span class="w5 h5 text-sm flex items-center justify-center rd-full bg-emerald-7 dark-bg-emerald-6 text-white">&check;</span>
                        Free optimazation.
                    </li>
                    <li class="flex items-center gap-x-4">
                        <span class="w5 h5 text-sm flex items-center justify-center rd-full bg-emerald-7 dark-bg-emerald-6 text-white">&check;</span>
                        Content Optimization.
                    </li>
                    <li class="flex items-center gap-x-4">
                        <span class="w5 h5 text-sm flex items-center justify-center rd-full bg-emerald-7 dark-bg-emerald-6 text-white">&check;</span>
                        Web site Analysis
                    </li>
                    <li class="flex items-center gap-x-4">
                        <span class="w5 h5 text-sm flex items-center justify-center rd-full bg-emerald-7 dark-bg-emerald-6 text-white">&check;</span>
                        Free optimazation.
                    </li>
                </ul>
            </div>
            <div class="flex md-flex-1">
                <img src="/images/working-on-housing-project.jpg" alt="working on housing" width="1300" class="wfull md-hfull object-cover rd-lg">
            </div>
        </div>
    </section>
</template>
<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>