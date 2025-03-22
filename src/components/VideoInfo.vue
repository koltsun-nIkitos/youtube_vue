<template>
  <div class="flex items-start mt-3">
    <img class="mr-3 rounded-full w-9 h-9" width="68px" alt="" 
      :src="getImageUrl('avatars', `avatar${index}.jpg`)"
    />
    
    <div class="text-sm">
      <span class="font-semibold text-gray-800">Video title {{ index }}</span>

      <div class="mt-1 flex items-center">
        <span>Chanel name {{ index }}</span>

        <BaseIcon 
          class="w-3.5 h-3.5 ml-1"
          name="checkCircle"
        />
      </div>

      <div v-html="summary"></div>
    </div>

    <button
      class="ml-auto -mt-1 p-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
    >
      <BaseIcon 
        class="w-6 h-6"
        name="dotsVertical"
      />
    </button>
  </div>
</template>


<script>
  import BaseIcon from './BaseIcon.vue';

  export default{
    components: {
      BaseIcon,
    },

    methods: {
      getImageUrl(folder, name) {
        return new URL(`../assets/img/${folder}/${name}`, import.meta.url).href;
      },
    },

    props: ["index"],

    computed: {
      summary(){
        const days = this.index === 1 ? 'day' : 'days'
        return `${this.index}K views &middot; ${this.index} ${days} before`
      },

    },
  }
</script>