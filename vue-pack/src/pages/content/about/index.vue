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
    link: [
        {
            href: "https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&display=swap",
            rel: "stylesheet"
        }
    ]
})


</script>
<template>
    <section class="py24">
        <div class="max-w-7xl mx-auto px-5 sm-px-10 md-px-12 lg-px-5 flex flex-col md-flex-row gap16">
            <div class="flex md-flex-1">
                <img src="/images/working-on-housing-project.jpg" alt="working on housing" width="1300"
                    class="wfull md-hfull object-cover rd-lg">
            </div>
            <div class="md-w-1/2 lg-w-54% space-y-12 text-gray-7 dark-text-gray-3">
                <h1 class="text-gray9 dark-text-white font-semibold text-2xl sm-text-3xl md-text-4xl">
                    We help drive your business forward faster
                </h1>
                <p>
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minus, saepe aliquid autem alias vero
                    distinctio dignissimos consequatur? Excepturi quibusdam, quam ipsum hic, laudantium ducimus suscipit,
                    culpa facere consequuntur repellat delectus.
                </p>
                <div class="grid sm-grid-cols-2 gap6">
                    <div class="space-y-6 p4 rd-xl bg-white dark-bg-gray-950 border border-gray1 dark-border-gray9">
                        <span class="rd-full bg-gray-9 dark-bg-gray1 text-gray1 dark-text-gray9 w-max p3 flex">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" class="w6 h6">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M9.813 15.904L9 18.75l-.813-2.846a4.5 4.5 0 00-3.09-3.09L2.25 12l2.846-.813a4.5 4.5 0 003.09-3.09L9 5.25l.813 2.846a4.5 4.5 0 003.09 3.09L15.75 12l-2.846.813a4.5 4.5 0 00-3.09 3.09zM18.259 8.715L18 9.75l-.259-1.035a3.375 3.375 0 00-2.455-2.456L14.25 6l1.036-.259a3.375 3.375 0 002.455-2.456L18 2.25l.259 1.035a3.375 3.375 0 002.456 2.456L21.75 6l-1.035.259a3.375 3.375 0 00-2.456 2.456zM16.894 20.567L16.5 21.75l-.394-1.183a2.25 2.25 0 00-1.423-1.423L13.5 18.75l1.183-.394a2.25 2.25 0 001.423-1.423l.394-1.183.394 1.183a2.25 2.25 0 001.423 1.423l1.183.394-1.183.394a2.25 2.25 0 00-1.423 1.423z" />
                            </svg>
                        </span>
                        <h2 class="font-semibold text-xl text-gray9 dark-text-white">Our mission</h2>
                        <p>
                            Lorem ipsum dolor sit amet consectetur
                        </p>
                    </div>

                    <div class="space-y-6 p-4 rd-xl bg-white dark-bg-gray-950 border border-gray1 dark-border-gray9">
                        <span class="rd-full bg-gray9 dark-bg-gray1 text-gray-1 dark-text-gray9 wmax p3 flex">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" class="w6 h6">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M2.036 12.322a1.012 1.012 0 010-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178z" />
                                <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                            </svg>
                        </span>
                        <h2 class="font-semibold text-xl text-gray-9 dark-text-white">Our vision</h2>
                        <p>
                            Lorem ipsum dolor sit amet consectetur
                        </p>
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