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
    <footer bg="white dark:gray-950" text="gray-7 dark:gray-3">
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto">
            <div border-t="~ gray-2 dark:gray-8" py="16 md:20" class="flex flex-col lg-flex-row gap-14 gap-y-16">
                <div class="w-full lg-w-96 space-y-6">
                    <nuxt-link to="#">
                        <span class="text-transparent bg-clip-text bg-gradient-to-tr from-blue-8 to-indigo-4 font-bold text-2xl">U</span>
                        Unify-Ui
                    </nuxt-link>
                    <p class="max-w-lg">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta iusto est quia a
                    </p>
                </div>
                <nav class="flex-1 grid grid-cols-2 md-grid-cols-4 gap-10">
                    <div v-for="footerItem in footerLinks" :key="footerItem.id" class="space-y-6">
                        <h1 un-text="lg gray-9 dark:gray-1" class="font-semibold">
                            {{ footerItem.title }}
                        </h1>
                        <ul class="space-y-3">
                            <li v-for="item in footerItem.items">
                                <nuxt-link :to="item.link" un-text="hover:blue-6 dark:hover:blue-5" class="duration-200">
                                    {{ item.label }}
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                </nav>
            </div>
        </div>
        <div bg="gray-1 dark:gray-9" class="py3">
            <div px="5 sm:10 md:12 lg:5" class="max-w-3xl mx-auto flex justify-center text-center">
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