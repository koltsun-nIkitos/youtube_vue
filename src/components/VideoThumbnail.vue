<template>
  <div class="relative">
    <img
      :src="getImageUrl('channels', `channel${index}.jpg`)"
      alt="Channel Image"
    />

    <span
      class="opacity-0 group-hover:opacity-100 bg-opacity-60 absolute top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
    >
    
      <BaseIcon
        name="clock"
        class="w-6 h-6"
      />
    </span>

    <span
      class="opacity-0 group-hover:opacity-100 bg-opacity-60 absolute top-9 right-0 bg-black text-white rounded-sm m-1 p-1"
    >
      <BaseIcon
        name="menuAlt3"
        class="w-6 h-6"
      />
    </span>

    <span class="opacity-100 group-hover:opacity-0 duration-500 bg-opacity-60 absolute bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-sm font-semibold">
      6:35
    </span>
  </div>
</template>

<script>
  import BaseIcon from './BaseIcon.vue';

  export default{
    components:{
      BaseIcon,
    },

  methods: {
    getImageUrl(folder, name) {
      return new URL(`../assets/img/${folder}/${name}`, import.meta.url).href;
    },
  },

  props: ["index"],
};
</script>
