<template>
  <section
    class="pt-14 md:pl-24 xl:pl-64 fixed bg-white z-10 w-full bg-opacity-95"
  >
    <div class="border-t border-b py-3 px-4 max-w-screen-2xl m-auto">
      <div
        class="no-scrollbar flex space-x-3 overflow-auto text-sm whitespace-nowrap"
      >
        <a
          v-for="category in categories"
          :key="category"
          href="#"
          class="px-3 transition py-1 bg-gray-600 border border-gray-700 rounded-full hover:bg-gray-500 text-white"
        >
          {{ category }}
        </a>
        
      </div>
    </div>
  </section>
</template>


<script>
export default{
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