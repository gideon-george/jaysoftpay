<template>
  <section class="relative">

    <!-- Dark background -->
    <div class="absolute inset-0  bg-blue-900 pointer-events-none -z-10 [clip-path:polygon(0_0,_5760px_0,_5760px_calc(100%_-_352px),_0_100%)]" aria-hidden="true"></div>

    <div class="relative max-w-6xl mx-auto px-4 sm:px-6">
      <div class="pt-32 pb-20 md:pt-40 md:pb-44">

        <!-- Hero content -->
        <div class="max-w-lg mx-auto md:max-w-none md:flex md:items-center md:space-x-8 lg:space-x-16 xl:space-x-20  md:space-y-0">

          <!-- Content -->
          <div class="text-center md:text-left md:min-w-[30rem]" data-aos="fade-right">
            <h2 class="h2 font-playfair-display text-slate-100 mb-4">Power your finance, grow your business</h2>
            <p class="text-xl text-slate-400 mb-8">Accept payments from customers. Automate payouts to vendors & employees. Never run out of working capital..</p>
            <div class="max-w-xs mx-auto sm:max-w-none sm:flex sm:justify-center md:justify-start space-y-4 sm:space-y-0 sm:space-x-4">
              <div>
                <router-link class="btn text-white bg-blue-600 hover:bg-blue-700 w-full group rounded" to="/request-demo">
                  Sign Up Now 
                  <span class="tracking-normal text-blue-300 group-hover:translate-x-0.5 transition-transform duration-150 ease-in-out ml-1">-&gt;</span>
                </router-link>
              </div>
            </div>
          </div>

          <!-- Hero image -->
        <!-- Hero image -->
          <div data-aos="fade-left">
            <!-- Image -->
            <div class="flex justify-center items-center">
              <div class="relative">
                <div class="absolute inset-0 pointer-events-none border-2 border-slate-700 mt-3 ml-3 translate-x-4 translate-y-4 -z-10" aria-hidden="true"></div>
                <img class="mx-auto md:max-w-none" src="../images/illustration-desktop.jpg" width="540" height="405" alt="Hero" />
              </div>
             
            </div>

            

          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
import { ref } from 'vue'

import Modal from './../utils/Modal.vue'

export default {
  name: 'HeroHome',
  components: {
    Modal,
  },
  setup() {

    const videoModalOpen = ref(false)

    return {
      videoModalOpen,
    }  
  }  
}
</script>