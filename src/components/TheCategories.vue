<template>
  <section
    :class="classes"
  >
    <div class="border-t border-b py-3 px-4 max-w-screen-2xl m-auto">
      <div
        class="no-scrollbar flex space-x-3 overflow-auto text-sm whitespace-nowrap"
      >
        <CategoryItem 
          v-for="category in categories"
          :key="category"
          :category="category"
          :is-active="category === 'All'"
        />
        
      </div>
    </div>
  </section>
</template>


<script>
import CategoryItem from './CategoryItem.vue';

export default{
  components:{
    CategoryItem
  },

  props:{
    isSidebarOpen: Boolean,
  },

  data() {
    return {
      categories: [
        'All',
        'Trucks',
        'Tools',
        'Machines',
        'Engines',
        'Show',
        'Ships',
        'Roads',
        'Thanks',
        'Building',
        'Mars',
        'Tractors',
        'TV Shows',
        'Football',
        'Planes',
        'Live',
        'Streets',
        'Math',
        'Programming',
      ]
    }
  },

  computed:{
    classes(){
      return [
        this.isSidebarOpen ? 'xl:pl-64' : 'md:pl-30',
        'pt-14', 
        'fixed', 
        'bg-white', 
        'z-10', 
        'w-full', 
        'bg-opacity-95',
      ]
    }
  }


}
</script>