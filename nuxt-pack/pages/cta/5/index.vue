<script setup>



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
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto relative">
            <div bg="white dark:gray-950" class="flex flex-col md-flex-row items-center text-center md-text-left md-justify-between gap-8 p12 rd-xl md-items-start">
                <div class="max-w-xl space-y-3">
                    <h1 text="2xl gray-9 dark:white" class="font-semibold">
                        Ready to take your skills to the noon
                    </h1>
                    <p text="gray-7 dark:gray-3">
                        Lorem ipsum dolor sit amet consectetur
                    </p>
                </div>
                <div class="flex items-center gap-3">
                    <nuxt-link to="#" un-bg="gray-2 dark:gray-8" un-text="gray-8 dark:gray-2" class="px5 py2.5 rd-lg">
                        Read doc
                    </nuxt-link>
                    <nuxt-link to="#" class="bg-blue-6 text-white px5 py2.5 rd-lg">
                        Get started
                    </nuxt-link>
                </div>
            </div>
        </div>
        <div bg="gray-9 dark:gray-8" class="pt32 -mt16"></div>
    </section>
</template>
<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>