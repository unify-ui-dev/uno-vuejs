<script setup>
useHead({
  title: 'Footer sections',
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


const footerLinks = [
  {
    id:1,
    title:"Services",
    items:[
      {
        id:1,
        label:'Marketing',
        link:'#'
      },
      {
        id:2,
        label:'Consultancy',
        link:'#'
      },
      {
        id:3,
        label:'Mobile Development',
        link:'#'
      },
      {
        id:4,
        label:'Mobile Development',
        link:'#'
      },
    ]
  },
  {
    id:2,
    title:"Company",
    items:[
      {
        id:1,
        label:'About',
        link:'#'
      },
      {
        id:2,
        label:'Carrer',
        link:'#'
      },
      {
        id:3,
        label:'Contact',
        link:'#'
      },
      {
        id:4,
        label:'Services',
        link:'#'
      },
    ]
  },
  {
    id:3,
    title:"Social",
    items:[
      {
        id:1,
        label:'Facebook',
        link:'#'
      },
      {
        id:2,
        label:'Twitter',
        link:'#'
      },
      {
        id:3,
        label:'Instagram',
        link:'#'
      },
      {
        id:4,
        label:'Linkedin',
        link:'#'
      },
    ]
  },
  {
    id:4,
    title:"Ressources",
    items:[
      {
        id:1,
        label:'Blog',
        link:'#'
      },
      {
        id:2,
        label:'Privacy',
        link:'#'
      },
      {
        id:3,
        label:'Terms',
        link:'#'
      },
      {
        id:4,
        label:'FAQ',
        link:'#'
      },
    ]
  }
]

</script>
<template>
    <footer bg="white dark:gray-950" un-text="gray-7 dark:gray-3">
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto py20 flex flex-col lg-flex-row gap-14">
            <div class="space-y-6 lg-w-96">
                <nuxt-link to="#">
                    <span
                        class="text-transparent bg-clip-text bg-gradient-to-tr from-blue-8 to-indigo-4 font-bold text-2xl">U</span>
                    Unify-Ui
                </nuxt-link>
                <p class="max-w-lg">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta iusto est quia a
                </p>
                <div class="flex w-full gap-5">
                    <nuxt-link to="#" aria-label="social link">
                        <span i-carbon-logo-twitter text-2xl flex></span>
                    </nuxt-link>
                    <nuxt-link to="#" aria-label="social link">
                        <span i-carbon-logo-linkedin text-2xl flex></span>
                    </nuxt-link>
                    <nuxt-link to="#" aria-label="social link">
                        <span i-carbon-logo-instagram text-2xl flex></span>
                    </nuxt-link>
                    <nuxt-link to="#" aria-label="social link">
                        <span i-carbon-logo-facebook text-2xl flex></span>
                    </nuxt-link>
                </div>
            </div>
            <nav class="lg-flex-1 grid grid-cols-2 md-grid-cols-4 gap-10">
                <div v-for="footerItem in footerLinks" :key="footerItem.id" class="space-y-6">
                    <h1 un-text="lg gray-9 dark:gray-1" class="font-semibold">
                        {{ footerItem.title }}
                    </h1>
                    <ul class="space-y-3">
                        <li v-for="item in footerItem.items" :key="item.id">
                            <nuxt-link :to="item.link" un-text="hover:blue-6 dark:hover:blue-5" class="duration-200">
                                {{ item.label }}
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto space-y-5">
            <div border-t="~ gray-1 dark:gray-9"
                class="py3 flex flex-col md-flex-row md-justify-between gap-6 md-items-center">
                <div text="gray-7 dark:gray-3" class="max-w-md space-y-3">
                    <h2 text="lg gray-9 dark:gray-1" class="font-semibold">
                        Join our news-letter
                    </h2>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    </p>
                </div>
                <div class="flex-1 max-w-md">
                    <form action="#" class="w-full flex flex-col sm-flex-row gap-3">
                        <input type="email" placeholder="johndoe@gmail.com" bg="gray-2 dark:gray-8"
                            class="px5 py2.5 rd-md outline-none flex-1">
                        <button
                            class="outline-none w-full py2.5 px5 sm-w-max bg-blue-6 text-white rd-md flex items-center justify-center">
                            Subscribe
                        </button>
                    </form>
                </div>
            </div>
            <div
                px="5 sm:10 md:12 lg:5" bg="gray-1 dark:gray-9" class="flex justify-center text-center py3 rd-md">
                <p> &copy; 2023 UnifyUI. All right reserved </p>
            </div>
        </div>
    </footer>
</template>
<style >
body{
    --at-apply: font-dms bg-white dark-bg-gray-950
}
</style>