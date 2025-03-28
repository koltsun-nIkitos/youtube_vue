<template>
  <main :class="classes">
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
    },

    props:{
      isSidebarOpen : Boolean,
    },

    computed:{
      classes(){
        return [
          this.isSidebarOpen ? 'xl:ml-64' : 'md:ml-30',
          'pt-32', 
          'px-5', 
          'sm:px-5', 
          'pb-5',
        ]
      }
    }

  };
</script>