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
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto flex flex-col items-start gap-10 xl-gap-14">
            <div class="text-center max-w-3xl mx-auto space-y-4">
                <h1 text="4xl gray-9 dark:white" class="font-semibold">
                    What we offer
                </h1>
                <p text="gray-7 dark:gray-3">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                </p>
            </div>
            <div class="grid sm-grid-cols-2 lg-grid-cols-3 gap-6 lg-gap-8">
                <div p="5 sm:6 lg:8" border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" class="rd-3xl relative overflow-hidden">
                    <div bg="gray-2 dark:gray-8" text="gray-9 dark:white" class="rd-xl p3 w-max relative">
                        <span i-carbon-tag-edit flex text-2xl></span> 
                    </div>
                    <div class="mt6 space-y-4 relative">
                        <h2 text="lg md:xl gray-9 dark:gray-1" class="font-semibold">
                            Social media marketing
                        </h2>
                        <p text="gray-7 dark:gray-3">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti qui soluta cupiditate
                        </p>
                    </div>
                    <span class="absolute w32 aspect-square -bottom-16 -right-16 bg-sky-6/10 rd-full"></span>
                </div>
                <div p="5 sm:6 lg:8" border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" class="rd-3xl relative overflow-hidden">
                    <div bg="gray-2 dark:gray-8" text="gray-9 dark:white" class="rd-xl p3 w-max relative">
                        <span i-carbon-email flex text-2xl></span> 
                    </div>
                    <div class="mt6 space-y-4 relative">
                        <h2 text="lg md:xl gray-9 dark:gray-1" class="font-semibold">
                            Email marketing
                        </h2>
                        <p text="gray-7 dark:gray-3">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti qui soluta cupiditate
                        </p>
                    </div>
                    <span class="absolute w32 aspect-square -bottom-16 -right-16 bg-sky-6/10 rd-full"></span>
                </div>
                <div p="5 sm:6 lg:8" border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" class="rd-3xl relative overflow-hidden">
                    <div bg="gray-2 dark:gray-8" text="gray-9 dark:white" class="rd-xl p3 w-max relative">
                        <span i-carbon-logo-glassdoor flex text-2xl></span>  
                    </div>
                    <div class="mt6 space-y-4 relative">
                        <h2 text="lg md:xl gray-9 dark:gray-1" class="font-semibold">
                            Social media marketing
                        </h2>
                        <p text="gray-7 dark:gray-3">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti qui soluta cupiditate
                        </p>
                    </div>
                    <span class="absolute w32 aspect-square -bottom-16 -right-16 bg-sky-6/10 rd-full"></span>
                </div>
                <div p="5 sm:6 lg:8" border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" class="rd-3xl relative overflow-hidden">
                    <div bg="gray-2 dark:gray-8" text="gray-9 dark:white" class="rd-xl p3 w-max relative">
                        <span i-carbon-tag-edit flex text-2xl></span>  
                    </div>
                    <div class="mt6 space-y-4 relative">
                        <h2 text="lg md:xl gray-9 dark:gray-1" class="font-semibold">
                            Social media marketing
                        </h2>
                        <p text="gray-7 dark:gray-3">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti qui soluta cupiditate
                        </p>
                    </div>
                    <span class="absolute w32 aspect-square -bottom-16 -right-16 bg-sky-6/10 rd-full"></span>
                </div>
                <div p="5 sm:6 lg:8" border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" class="rd-3xl relative overflow-hidden">
                    <div bg="gray-2 dark:gray-8" text="gray-9 dark:white" class="rd-xl p3 w-max relative">
                        <span i-carbon-tag-edit flex text-2xl></span>  
                    </div>
                    <div class="mt6 space-y-4 relative">
                        <h2 text="lg md:xl gray-9 dark:gray-1" class="font-semibold">
                            Email marketing
                        </h2>
                        <p text="gray-7 dark:gray-3">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti qui soluta cupiditate
                        </p>
                    </div>
                    <span class="absolute w32 aspect-square -bottom-16 -right-16 bg-sky-6/10 rd-full"></span>
                </div>
                <div p="5 sm:6 lg:8" border="~ gray-2 dark:gray-8" bg="gray-1 dark:gray-9" class="rd-3xl relative overflow-hidden">
                    <div bg="gray-2 dark:gray-8" text="gray-9 dark:white" class="rd-xl p3 w-max relative">
                        <span i-carbon-tag-edit flex text-2xl></span>  
                    </div>
                    <div class="mt6 space-y-4 relative">
                        <h2 text="lg md:xl gray-9 dark:gray-1" class="font-semibold">
                            Social media marketing
                        </h2>
                        <p text="gray-7 dark:gray-3">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corrupti qui soluta cupiditate
                        </p>
                    </div>
                    <span class="absolute w32 aspect-square -bottom-16 -right-16 bg-sky-6/10 rd-full"></span>
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