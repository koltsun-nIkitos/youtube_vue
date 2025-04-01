<template>
  <div class="flex items-start mt-3">
    <img class="mr-3 rounded-full w-9 h-9" width="68px" alt="" 
      :src="getImageUrl('avatars', `avatar${index}.jpg`)"
    />
    
    <div class="text-sm">
      <span class="font-semibold text-gray-800">Video title {{ index }}</span>

      <div class="mt-1 flex">
        <BaseTooltip text="channelName" top>
          <span>{{ channelName }}</span>
        </BaseTooltip>

        <BaseTooltip text="Verified" top>
          <BaseIcon 
            class="w-3.5 h-3.5 ml-1"
            name="checkCircle"
          />
        </BaseTooltip>
      </div>

      <div v-html="summary"></div>
    </div>

    <VideoDropdown />
  </div>
</template>


<script>
  import BaseIcon from './BaseIcon.vue';
  import VideoDropdown from './VideoDropdown.vue';
  import BaseTooltip from './BaseTooltip.vue'

  export default{
    data(){
      return{
        channelName: `Chanel name ${this.index}`,
      }
    },

    components: {
      BaseIcon,
      VideoDropdown,
      BaseTooltip,
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