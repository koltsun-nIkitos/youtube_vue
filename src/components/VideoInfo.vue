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

    <VideoDropdown />
  </div>
</template>


<script>
  import BaseIcon from './BaseIcon.vue';
  import VideoDropdown from './VideoDropdown.vue';

  export default{
    components: {
      BaseIcon,
      VideoDropdown,
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