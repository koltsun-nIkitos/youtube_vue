<template>
  <main class="md:ml-24 xl:ml-64 pt-32 px-5 sm:px-5 pb-5">
    <div
      class="grid gap-4 sm:grid-cols-2 lg:grid-cols-3 xl:grid-4 2xl:grid-cols-5 max-w-screen-2xl m-auto"
    >
      <TheVideo v-for="i in 16" :key="i" :index="i"/>

    </div>
  </main>
</template>


<script>
  import TheVideo from './TheVideo.vue';

  export default {

    components:{
      TheVideo
    }

  };
</script>