<template>
  <aside
    :class="classes"
  >
    <section>
      <ul>
        <SidebarCompactItem 
          v-for="navItem in navItems"
          :key="navItem.label"
          :icon="navItem.icon" 
          :label="navItem.label" 
          :is-active="navItem.isActive"
        />
        
      </ul>
    </section>
  </aside>
</template>


<script>
  import SidebarCompactItem from './SidebarCompactItem.vue'


export default{
  components: {
    SidebarCompactItem
  },

  data(){
    return {
      navItems : [
        {label: 'Home', icon: 'home', isActive: true},
        {label: 'Trending', icon: 'fire', isActive: false},
        {label: 'Subscriptions', icon: 'collection', isActive: false},
        {label: 'Library', icon: 'duplicate', isActive: false},
        {label: 'History', icon: 'clock', isActive: false},
      ]
    }
    
  },

  computed:{
    classes(){
      return[
        'min-h-screen', 
        'no-scrollbar', 
        'overflow-auto', 
        'fixed ', 
        'top-0',
        'pt-14', 
        'bg-white', 
        'z-20',
      ]
    }
  },
}
</script>