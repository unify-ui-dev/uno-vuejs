<script setup>
import { useHead } from 'unhead'


useHead({
  title: 'Metric sections',
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
    <section class="py24">
        <div class="max-w-4xl mx-auto px-5 sm-px10 md-px12 lg-px5">
            <div class="p6 rd-lg bg-gray1 dark-bg-gray9 grid sm-grid-cols-2 lg-grid-cols-4 gap4 text-center">
                <div class="space-y2">
                    <h2 class="text-3xl sm-text-4xl lg-text-5xl font-semibold text-gray9 dark-text-white">
                        20+
                    </h2>
                    <p class="text-gray7 dark-text-gray3">
                        Projects
                    </p>
                </div>
                <div class="space-y2">
                    <h2 class="text-3xl sm-text-4xl lg-text-5xl font-semibold text-gray9 dark-text-white">
                        4
                    </h2>
                    <p class="text-gray7 dark-text-gray3">
                        Years Experience
                    </p>
                </div>
                <div class="space-y2">
                    <h2 class="text-3xl sm-text-4xl lg-text-5xl font-semibold text-gray9 dark-text-white">
                        10+
                    </h2>
                    <p class="text-gray7 dark-text-gray3">
                        Clients
                    </p>
                </div>
                <div class="space-y2">
                    <h2 class="text-3xl sm-text-4xl lg-text-5xl font-semibold text-gray9 dark-text-white">
                        98%
                    </h2>
                    <p class="text-gray7 dark-text-gray3">
                        Satisfaction
                    </p>
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