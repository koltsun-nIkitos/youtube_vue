<template>
  <span
    :class="classes" @mouseenter="toogleBage" @mouseleave="toogleBage"
  >
    <BaseIcon :name="icon" class="w-6 h-6" />
    <span :class="badgeClasses">
      <span class="inline-block my-2 mx-3">{{ label }}</span>
    </span>
  </span>
</template>


<script>
import BaseIcon from './BaseIcon.vue';

export default{
  components:{
    BaseIcon
  },

  props:{
    icon: String,
    label: String,
  },

  data(){
    return{
      isBageShown: false,
    }
  },

  computed:{
    classes(){
      return[
        'opacity-0', 
        'group-hover:opacity-100', 
        'bg-opacity-60', 
        'absolute top-0', 
        'right-0', 
        'bg-black', 
        'text-white', 
        'm-1', 
        'p-1',
        this.isBageShown ? 'rounded-r-sm' : 'rounded-sm', 
      ]
    },

    badgeClasses(){
      return[
        'absolute',
        'transition-width', 
        'bg-black', 
        'bg-opacity-60', 
        'whitespace-nowrap', 
        'top-0', 
        'right-full', 
        'oveflow-hidden', 
        'uppercase', 
        'text-xs', 
        'delay-100', 
        'font-semibold', 
        'rounded-l-sm', 
        this.isBageShown ? 'w-28' : 'w-0', 
        this.isBageShown ? 'opacity-100' : 'opacity-0',
      ]
    }
  },

  methods:{
    toogleBage(){
      this.isBageShown = !this.isBageShown
    }
  }
}
</script>