<template>
  <div class="relative">
    <img
      :src="getImageUrl('channels', `channel${index}.jpg`)"
      alt="Channel Image"
    />

    <VideoThumbnailButton icon="clock" label="watch later" class="top-0"/>

    <VideoThumbnailButton icon="menuAlt3" label="Add to queque" class="top-10"/>


    <span class="opacity-100 group-hover:opacity-0 duration-500 bg-opacity-60 absolute bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-sm font-semibold">
      6:35
    </span>
  </div>
</template>

<script>
  import BaseIcon from './BaseIcon.vue';
  import VideoThumbnailButton from './VideoThumbnailButton.vue';

  export default{
    components:{
      BaseIcon,
      VideoThumbnailButton
    },

  methods: {
    getImageUrl(folder, name) {
      return new URL(`../assets/img/${folder}/${name}`, import.meta.url).href;
    },
  },

  props: ["index"],
};
</script>
