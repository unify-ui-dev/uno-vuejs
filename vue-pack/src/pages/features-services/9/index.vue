<script setup>
import { useHead } from 'unhead'


useHead({
  title: 'Feaure & Services',
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
    <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto">
      <div class="flex flex-col space-y-16">
        <div class="flex flex-col justify-center text-center  mx-auto md-max-w-3xl space-y-5">
          <span bg="blue-50 dark:gray-9" text="xs emerald-8 dark:gray-1"
            class="rd-lg px-2.5 py-1 w-max mx-auto font-semibold tracking-wide">Features</span>
          <h1 text="3xl md:4xl xl:5xl blue-950 dark:gray-2" class="font-semibold leading-tight">
            The tool that changes your day-to-day management
          </h1>
          <p text="gray-7 dark:gray-3" class="max-w-lg mx-auto">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quae odio consequatur aliquam ratione quod iusto
            aspernatur
          </p>
        </div>
        <div class="grid gap-14 md-grid-cols-2 lg-grid-cols-4 lg-items-center">
          <div class="order-1 grid gap-10 sm-grid-cols-2 md-order-1 md-grid-cols-1 lg-order-1">
            <div class="flex flex-col space-y-6 justify-center md-justify-start">
              <span bg="blue-50 dark:gray-9" text="blue-7 dark:blue-5" class="p2 rd-md flex w-max">
                <!-- feature icon -->
                <span i-carbon-ibm-watson-openscale flex text-xl></span>
              </span>
              <h1 text="lg gray-9 dark:white" class="flex font-semibold capitalize">
                Feature 1
              </h1>
              <p text="sm gray-7 dark:gray-3" class="font-light">
                Lorem Ipsum is simply dummy text of the printing and type setting industry. Industry's standard dummy
              </p>
            </div>
            <div class="flex flex-col space-y-6 justify-center md-justify-start">
              <span bg="blue-50 dark:gray-9" text="blue-7 dark:blue-5" class="p2 rd-md flex w-max">
                <!-- feature icon -->
                <span i-carbon-ibm-watson-openscale flex text-xl></span>
              </span>
              <h1 text="lg gray-9 dark:white" class="flex font-semibold capitalize">
                Feature 1
              </h1>
              <p text="sm gray-7 dark:gray-3" class="font-light">
                Lorem Ipsum is simply dummy text of the printing and type setting industry. Industry's standard dummy
              </p>
            </div>
          </div>
          <div class="flex items-center justify-center order-3 md-col-span-2 lg-order-2 lg-row-span-2 lg-h-full">
            <div class="flex items-center justify-center order-3 md-col-span-2 lg-order-2 lg-row-span-2 lg-h-full">
              <div
                class="flex-1 relative bg-gradient-to-tr from-sky-1 to-indigo-3 p6 rd-lg aspect-[4/2.4] overflow-hidden">
                <img src="/images/dash-light.webp" alt="illustration" width="1800" class="wfull hauto">
              </div>
            </div>
          </div>
          <div class="order-1 grid gap-10 sm-grid-cols-2 md-order-2 md-grid-cols-1 lg-order-3">
            <div class="flex flex-col space-y-6 justify-center md-justify-start">
              <span bg="blue-50 dark:gray-9" text="blue-7 dark:blue-5" class="p2 rd-md flex w-max">
                <!-- feature icon -->
                <span i-carbon-ibm-watson-openscale flex text-xl></span>
              </span>
              <h1 text="lg gray-9 dark:white" class="flex font-semibold capitalize">
                Feature 1
              </h1>
              <p text="sm gray-7 dark:gray-3" class="font-light">
                Lorem Ipsum is simply dummy text of the printing and type setting industry. Industry's standard dummy
              </p>
            </div>
            <div class="flex flex-col space-y-6 justify-center md-justify-start">
              <span bg="blue-50 dark:gray-9" text="blue-7 dark:blue-5" class="p2 rd-md flex w-max">
                <!-- feature icon -->
                <span i-carbon-ibm-watson-openscale flex text-xl></span>
              </span>
              <h1 text="lg gray-9 dark:white" class="flex font-semibold capitalize">
                Feature 1
              </h1>
              <p text="sm gray-7 dark:gray-3" class="font-light">
                Lorem Ipsum is simply dummy text of the printing and type setting industry. Industry's standard dummy
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style >
body {
  --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>