<script setup>
useHead({
  title: 'Testimonial',
  meta: [
    {
      name: 'description',
      content: 'Testimonials',
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
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto space-y-16">
            <div class="space-y-4 max-w-2xl">
                <span un-before="absolute content-empty w4 h0.5 rd-md left-0 top-1/2 bg-sky-7 dark:bg-sky-6" text="sky-7 dark:sky-5" class="pl5 relative">
                    Happy Clients
                </span>
                <h2 text="3xl blue-950 dark:gray-2" class="font-semibold leading-tight">Client’s Say About Us</h2>
            </div>
            <div
                class="relative">
                <div class="flex md=items-stretch gap-10 lg=gap-14">
                    <div class="hidden md-flex md-w1/2 lg-w2/5 md-h-auto">
                        <img src="/images/sidebiew.webp" alt="Author Avatr" class="w-full h-full object-cover rd-lg">
                    </div>
                    <div class="flex-1 flex flex-col space-y-6 md-space-y-12 lg-space-y-16 md-py-6 lg-py-8 md-h-auto md-justify-center">
                        <p text="xl lg:2xl gray-7 dark:gray-3" class="font-medium">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum at ipsa pariatur culpa iste dolore aliquid officia modi quas vel inventore animi, error commodi distinctio eum accusamus? Accusantium, tempora quisquam!
                        </p>
                        <div class="flex items-start gap-4">
                            <img src="/images/sidebiew.webp" alt="Author avatar" class="w12 h12 rd-full flex md-hidden">
                            <div class="space-y-1 flex-1">
                                <h2 text="lg gray-8 dark:gray-2" class="font-semibold leading-none">
                                    John Doe
                                </h2>
                                <p text="gray-6 dark:gray-4">
                                    SEO Kelasi-AI SARL
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
                <div bg="gray-1 dark:gray-9" class="md-absolute md-right-0 md-bottom-6 lg-bottom-8 p1 rd-lg flex items-start gap-3 w-max mt10 md-mt0">
                    <button aria-label="Prev Button" text="gray-7 dark:gray-3" bg="gray-2 dark:gray-8 hover:white dark:hover:gray-950" class="outline-none p2.5 rd-md transition ease-linear">
                        <span i-carbon-arrow-left text-xl flex></span>                         
                    </button>
                    <button aria-label="Next Button" text="gray-7 dark:gray-3" bg="gray-2 dark:gray-8 hover:white dark:hover:gray-950" class="outline-none p2.5 rd-md transition ease-linear">
                        <span i-carbon-arrow-right text-xl flex></span>                                                  
                    </button>
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