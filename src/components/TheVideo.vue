<template>
  <a href="./channel.html" class="mb-7 group">
    <VideoThumbnail :index="index"/>
    
    <VideoInfo :index="index"/>
  </a>
</template>


<script>
  import VideoThumbnail from './VideoThumbnail.vue';
  import VideoInfo from './VideoInfo.vue';

  export default {
    components: {
      VideoThumbnail,
      VideoInfo,
    },

    props: ['index'],
  };

  
</script>