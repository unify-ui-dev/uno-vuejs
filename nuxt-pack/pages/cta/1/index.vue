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
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto">
            <div p="8 md:10 y14 lg:14" class="bg-gradient-to-br from-blue-2 to-gray-50 dark-from-gray-9 dark-bg-gray-8 rd-lg flex flex-col md-flex-row items-center justify-center text-center md-text-left md-justify-start md-items-start gap-8">
                <div class="md:w-2/5">
                    <h1 text="3xl sm:4xl md:5xl xl:6xl blue-950 dark:white" class="font-display font-bold leading-tight">
                        Ready to grow your business?
                    </h1>
                </div>
                <div class="flex flex-col md-flex-1 space-y-8">
                    <p text="gray-7 dark:gray-3">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas numquam hic odit ducimus pariatur deleniti voluptatibus delectus vero, alias debitis quae cumque eum
                    </p>
                    <div class="flex justify-center md-justify-start">
                        <nuxt-link to="#" class="h12 px5 rd-md flex items-center bg-blue-6 text-white">
                            Get In Touch
                        </nuxt-link>
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