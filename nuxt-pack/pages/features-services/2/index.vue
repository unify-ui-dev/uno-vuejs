<script setup>



useHead({
  title: 'Feaure & Services',
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
    <section py-20>
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto flex flex-col md-flex-row gap-10 xl-gap-14">
            <div class="flex flex-1 flex-col gap-5">
                <div class="flex flex-col gap-5">
                    <div class="flex flex-col">
                        <h2 text="4xl lg:4xl gray-8 dark:white" class="font-bold">
                            We are offering best delivery services in Lubumbashi
                        </h2>
                    </div>
                    <p text="gray-7 dark:gray-3">Lorem ipsum dolor sit amet consectetur adipisicing
                        elit.</p>
                </div>
                <div class="space-y-3">
                    <div
                         bg="white dark:gray-950" shadow="lg dark:none transparent hover:emerald-6/20" border="~ gray-1 hover:gray-1 dark:gray-9 dark:hover:gray-6" class="p3 rd-md transition-all ease-linear">
                        <div class="flex gap-4">
                            <div class="min-w-max">
                                <span
                                    text="emerald-6 dark:gray-1" bg="emerald-6/10 dark:gray-9" class="rd flex aspect-square p3">
                                    <span i-carbon-restaurant flex text-2xl></span>
                                </span>
                            </div>
                            <div class="space-y-0.5">
                                <h3 text="lg gray-9 dark:gray-1" class="font-semibold">
                                    Feature
                                </h3>
                                <p text="gray-6 dark:gray-4" class="line-clamp-2">
                                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est animi reiciendis
                                    laboriosam aut
                                </p>
                            </div>
                        </div>
                    </div>

                    <div
                        bg="white dark:gray-950" shadow="lg dark:none transparent hover:emerald-6/20" border="~ gray-1 hover:gray-1 dark:gray-9 dark:hover:gray-6" class="p3 rd-md transition-all ease-linear">
                        <div class="flex gap-4">
                            <div class="min-w-max">
                                <span
                                    text="emerald-6 dark:gray-1" bg="emerald-6/10 dark:gray-9" class="rd flex aspect-square p3">
                                    <span i-carbon-restaurant-fine flex text-2xl></span>
                                </span>
                            </div>
                            <div class="space-y-0.5">
                                <h3 text="lg gray-9 dark:gray-1" class="font-semibold">
                                    Feature
                                </h3>
                                <p text="gray-6 dark:gray-4" class="line-clamp-2">
                                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est animi reiciendis
                                    laboriosam aut
                                </p>
                            </div>
                        </div>
                    </div>
                    <div
                        bg="white dark:gray-950" shadow="lg dark:none transparent hover:emerald-6/20" border="~ gray-1 hover:gray-1 dark:gray-9 dark:hover:gray-6" class="p3 rd-md transition-all ease-linear">
                        <div class="flex gap-4">
                            <div class="min-w-max">
                                <span
                                    text="emerald-6 dark:gray-1" bg="emerald-6/10 dark:gray-9" class="rd flex aspect-square p3">
                                    <span i-carbon-restaurant flex text-2xl></span>
                                </span>
                            </div>
                            <div class="space-y-0.5">
                                <h3 text="lg gray-9 dark:gray-1" class="font-semibold">
                                    Feature
                                </h3>
                                <p text="gray-6 dark:gray-4" class="line-clamp-2">
                                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est animi reiciendis
                                    laboriosam aut
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div
                class="w-full md-h-auto object-cover flex md-items-end justify-center md-w-1/2 xl-w-45% relative">
                <div class="absolute inset-x-0 bottom-0 h1/4 bg-gradient-to-tr from-gray-1 to-gray-3 dark-from-gray-9 dark-to-gray-7 rd-3xl"></div>
                <img src="/images/woman-with-gro.webp" width="1001" height="1001" alt="woman with grocery" class="wfull hauto lg-w86% relative">
            </div>

        </div>
    </section>
</template>
<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>