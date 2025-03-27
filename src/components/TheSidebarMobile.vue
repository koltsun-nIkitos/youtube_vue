<template>
  <transition
    enter-active-class="transition-opacity ease-linear duration-200"
    enter-from-class="opacity-0"
    enter-to-class="opacity-100"
    leave-active-class="transition-opacity ease-linear duration-200"
    leave-from-class="opacity-100"
    leave-to-class="opacity-0"
  >

    <TheSidebarMobileOverlay v-show="isOpen" @click="isOpen = false"> 

    </TheSidebarMobileOverlay>
  </transition>

  <transition
    enter-active-class="transition ease-in-out duration-200 transform"
    enter-from-class="-translate-x-full"
    enter-to-class="translate-x-0"
    leave-active-class="transition ease-in-out duration-200 transform"
    leave-from-class="translate-x-0"
    leave-to-class="-translate-x-full"
  >
    <aside v-show="isOpen" class="no-scrollbar   w-64 max-h-screen overflow-auto bg-white fixed z-40">
      <section
        class="flex items-center p-4 border-b sticky top-0 bg-white z-30"
      >
        <button @click="isOpen = false" class="ml-2 mr-6 focus:outline-none">
          <BaseIcon name="menu" />
        </button>

        <logoMain />
      </section>

      <SidebarContent />
    </aside>
  </transition>

  
</template>

<script>
import TheSidebarMobileOverlay from './TheSidebarMobileOverlay.vue'
import BaseIcon from './BaseIcon.vue'
import LogoMain from './LogoMain.vue'
import SidebarContent from './SidebarContent.vue'

export default{
  components:{
    TheSidebarMobileOverlay,
    BaseIcon,
    LogoMain,
    SidebarContent,

  },

  data(){
    return {
      isOpen: true
    }
  },
}
</script>