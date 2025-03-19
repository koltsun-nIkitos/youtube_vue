<template>
  <section
    class="pt-14 md:pl-24 xl:pl-64 fixed bg-white z-10 w-full bg-opacity-95"
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


}
</script>