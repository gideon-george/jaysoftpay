<template>
  <header class="absolute w-full z-30" :class="{ 'dark': mode !== 'light' }">
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="flex items-center justify-between h-16 md:h-20">

        <!-- Site branding -->
        <div class="shrink-0 mr-4">
          <!-- Logo -->
          <router-link class="block text-blue-900 transition duration-150 ease-in-out" to="/" aria-label="Cruip">
           <span class="text-white font-bold text-2xl ">Jaysoftpay</span>
          </router-link>
        </div>

        <!-- Desktop navigation -->
        <nav class="hidden md:flex md:grow">

          <!-- Desktop menu links -->
          <ul class="flex grow justify-start flex-wrap items-center">
            <li>
              <router-link to="/#" class="font-medium text-indigo-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Payments</router-link>
            </li>
            <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Banking Plus</router-link>
            </li>
            <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Rize</router-link>
            </li>
            <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Resources</router-link>
            </li>
               <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Partners</router-link>
            </li>
            <!-- 1st level: hover -->
            <Dropdown title="support">
              <li>
                <router-link to="/404" class="font-medium text-sm text-slate-600 hover:text-blue-600 flex py-2 px-5 leading-tight">404</router-link>
              </li>
              <li>
                <router-link to="/support" class="font-medium text-sm text-slate-600 hover:text-blue-600 flex py-2 px-5 leading-tight">Support center</router-link>
              </li>
            </Dropdown>
          </ul>

          <!-- Desktop sign in links -->
          <ul class="flex grow justify-end flex-wrap items-center">
            <li>
              <router-link to="/signin" class=" border-2 border-blue-100 font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Sign in</router-link>
            </li>
             <li>
              <router-link to="/signin" class=" m-3 bg-gray-100 font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Sign up</router-link>
            </li>
          </ul>

        </nav>

        <!-- Mobile menu -->
        <div class="flex md:hidden">

          <!-- Hamburger button -->
          <button class="hamburger" ref="hamburger" :class="{ active: mobileNavOpen }" aria-controls="mobile-nav" :aria-expanded="mobileNavOpen" @click="mobileNavOpen = !mobileNavOpen">
            <span class="sr-only">Menu</span>
            <svg class="w-6 h-6 fill-current text-slate-900 dark:text-slate-100" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <rect y="4" width="24" height="2" />
              <rect y="11" width="24" height="2" />
              <rect y="18" width="24" height="2" />
            </svg>
          </button>

          <!-- Mobile navigation -->
          <transition
            enter-active-class="transition ease-out duration-200 transform"
            enter-from-class="opacity-0 -translate-y-2"
            enter-to-class="opacity-100 translate-y-0"
            leave-active-class="transition ease-out duration-200"
            leave-from-class="opacity-100"
            leave-to-class="opacity-0"
          >
            <nav
              id="mobile-nav"
              ref="mobileNav"
              v-show="mobileNavOpen"
              class="absolute top-full h-screen pb-16 z-20 left-0 w-full overflow-scroll no-scrollbar bg-white"
            >
              <ul class="px-5 py-2">
                <li>
              <router-link to="/#" class="font-medium text-indigo-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Payments</router-link>
            </li>
            <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Banking Plus</router-link>
            </li>
            <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Rize</router-link>
            </li>
            <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Resources</router-link>
            </li>
               <li>
              <router-link to="/#" class="font-medium text-slate-800 hover:text-blue-600 dark:text-slate-400 dark:hover:text-blue-600 px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out">Partners</router-link>
            </li>             
                <li class="py-2 my-2 border-t border-b border-slate-200">
                  <span class="flex font-medium text-slate-800 hover:text-blue-600 py-2">Resources</span>
                  <ul class="pl-4">
                    <li>
                      <router-link to="/404" class="text-sm flex font-medium text-slate-600 hover:text-blue-600 py-2">404</router-link>
                    </li>
                    <li>
                      <router-link to="/support" class="text-sm flex font-medium text-slate-600 hover:text-blue-600 py-2">Support</router-link>
                    </li>
                  </ul>
                </li>
                <li>
                  <router-link to="/signin" class="flex font-medium w-full text-slate-800 hover:text-blue-600 py-2">Sign in</router-link>
                </li>
    <li>
                  <router-link to="/signin" class="flex font-medium w-full text-slate-800 hover:text-blue-600 py-2">Sign Up</router-link>
                </li>
              </ul>
            </nav>
          </transition>

        </div>

      </div>
    </div>
  </header>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue'
import Dropdown from './../utils/Dropdown.vue'

export default {
  name: 'Header',
  props: ['mode'],
  components: {
    Dropdown,
  },
  setup() {

    const mobileNavOpen = ref(false)
    const mobileNav = ref(null)
    const hamburger = ref(null)

    // close on click outside
    const clickHandler = ({ target }) => {
      if (!mobileNavOpen.value || mobileNav.value.contains(target) || hamburger.value.contains(target)) return
      mobileNavOpen.value = false
    }

    // close if the esc key is pressed
    const keyHandler = ({ keyCode }) => {
      if (!mobileNavOpen.value || keyCode !== 27) return
      mobileNavOpen.value = false
    }  
    
    onMounted(() => {
      document.addEventListener('click', clickHandler)
      document.addEventListener('keydown', keyHandler)
    })

    onUnmounted(() => {
      document.removeEventListener('click', clickHandler)
      document.removeEventListener('keydown', keyHandler)
    })        

    return {
      mobileNavOpen,
      mobileNav,
      hamburger,
    }    
  }
}
</script>