<script setup>
const sidebarIsToggled = useState('sidebarIsToggled',()=>false)
const toggleSidebar = () => {
  sidebarIsToggled.value = !sidebarIsToggled.value
  if (!sidebarIsToggled) {
    document.body.classList.toggle("overflow-y-auto")
  } else {
    document.body.classList.add("overflow-y-auto")
  }
}


useHead({
  title: 'Sidebar',
  meta: [
    {
      name: 'description',
      content: 'Sidebar',
    },
  ],
  link: [
    {
      href: "https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap",
      rel: "stylesheet"
    }
  ]
})


const navGroup = [
  {
    id: 1,
    icon: 'i-carbon-home',
    label: 'Home',
    link: '#',
    isActive: true
  },
  {
    id: 2,
    icon: 'i-carbon-user-multiple',
    label: 'Users',
    link: '#',
    isActive: false
  },
  {
    id: 3,
    icon: 'i-carbon-shopping-cart',
    label: 'Sales',
    link: '#',
    isActive: false
  },
  {
    id: 4,
    icon: 'i-carbon-analytics',
    label: 'Analytics',
    link: '#',
    isActive: false
  },
]

const navItems = [
  {
    id: 1,
    icon: 'i-carbon-task',
    text: 'Tasks',
    link: '/',
  },
  {
    id: 2,
    icon: 'i-carbon-calendar',
    text: 'Calendar',
    link: '/'
  },
  {
    id: 3,
    icon: 'i-carbon-notification',
    text: 'Notifications',
    link: '/'
  },
  {
    id: 4,
    icon: 'i-carbon-analytics',
    text: 'Analytics',
    link: '/'
  },
]


</script>
<template>
  <aside bg="white dark:gray-950" border-r="~ gray-1 dark:gray-9"
    class="fixed h-[100dvh] overflow-hidden lg-relative w11/12 max-w-[20rem] md-w80 transition-all flex lg-transition-none ease-linear "
    :class="{
      'translate-x-0': sidebarIsToggled,
      '-translate-x-full lg-translate-x-0': !sidebarIsToggled
    }">
    <nav
      class="w-[4.2rem] p-2 border-r border-r-gray-100 dark:border-r-gray-900 flex flex-col justify-between gap-5 items-center">
      <div border-b="~ gray-1 dark:gray-9" class="flex w-full pb2">
        <nuxt-link to="#" class="bg-blue-6 w-full aspect-square rd-md flex items-center justify-center text-white">
          <span i-carbon-shopping-cart-plus text-2xl></span>
        </nuxt-link>
      </div>
      <ul class="flex flex-col w-full gap-4 flex-1">
        <li v-for="item in navGroup" :key="item.id" class="flex w-full">
          <nuxt-link :to="item.link"
            class="text-gray-9 dark-text-gray-1 w-full flex items-center justify-center aspect-square rd-md"
            :class="{ 'bg-gray-1 dark-bg-gray-9': item.isActive }">
            <span class="text-2xl" :class="item.icon"></span>
            <span class="sr-only">{{ item.label }}</span>
          </nuxt-link>
        </li>
      </ul>
      <div class="min-h-max w-full">
        <button aria-label="log out" un-text="gray-7 dark:gray-3" un-bg="transparent hover:gray-1 dark:hover:gray-9"
          class="outline-none flex items-center justify-center aspect-square w-full rd-md">
          <span i-carbon-logout text-2xl></span>
        </button>
      </div>
    </nav>
    <div class="flex-1 p2">
      <nav class="flex flex-col gap-4">
        <div border-b="~ gray-1 dark:gray-9" class="pt3 pb3">
          <form class="w-full relative">
            <span un-text="gray-6 dark:gray-4" class="absolute left-3 inset-y-2 flex items-center">
              <span i-carbon-search flex text-xl></span>
            </span>
            <input type="search" placeholder="Type something" un-text="gray-7 dark:gray-3 sm"
              un-bg="gray-1 dark:gray-9 focus:gray-50 dark:focus:gray-950" border="~ gray-2 dark:gray-8"
              class="w-full outline-none rd-md pl10 pr4 py2.5">
          </form>
        </div>
        <ul class="flex flex-col gap-3">
          <li v-for="item in navItems" :key="item.id">
            <nuxt-link :to="item.link" class="text-gray-7 dark-text-gray-3 flex items-center gap-x-3 px4 py2.5 rd-md">
              <span class="text-2xl" :class="item.icon"></span>
              {{ item.text }}
            </nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
  </aside>
  <main>
    <div class="flex lg-hidden fixed right-2 top2 p4">
      <button @click="toggleSidebar" un-bg="blue-6 dark:blue-5"
        class="p3 rd-full outline-none w12 aspect-square flex flex-col relative justify-center items-center"
        aria-label="toggle sidebar">
        <span class="w6 h0.5 rd-full bg-gray-3 transition-transform duration-300 ease-linear"
          :class="sidebarIsToggled ? 'translate-y-1.5 rotate-40' : ''"></span>
        <span class="w6 origin-center  mt-1 h-0.5 rd-full bg-gray-3 transition-all duration-300 ease-linear"
          :class="sidebarIsToggled ? 'scale-x-0 op-0' : ''"></span>
        <span class="w6 mt1 h0.5 rd-full bg-gray-3 transition-all duration-300 ease-linear"
          :class="sidebarIsToggled ? '-translate-y-1.5 -rotate-40' : ''"></span>
      </button>
    </div>
  </main>
</template>
<style >
body {
  --at-apply: font-inter bg-white dark-bg-gray-950
}
</style>