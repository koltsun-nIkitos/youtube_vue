<template>
  <aside :class="classes">
    <SidebarContent />
  </aside>
</template>


<script>
  import SidebarContent from './SidebarContent.vue';

  export default{
    components: {
      SidebarContent

    },

    props: {
      isOpen: Boolean,
    },

    computed: {
      classes(){
        return [
          this.isOpen ? 'xl:block' : 'hidden',
          'no-scrollbar', 
          'w-64', 
          'max-h-screen', 
          'overflow-auto', 
          'fixed', 
          'top-0', 
          'pt-12', 
          'bg-white', 
          'z-20',
        ]
      }
    },
  }
</script>