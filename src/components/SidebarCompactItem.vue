<template>
  <li>
    <a
      href="#"
      :class="classes"
    >
      <BaseIcon :name="icon" class="2-6 h-6 mb-2" />
      
      <span class="text-xs">{{ label }}</span>
    </a>
  </li>
</template>


<script>
import BaseIcon from './BaseIcon.vue'


export default{
  components:{
    BaseIcon,
  },

  props:{
    icon: String, 
    label: String,
    isActive: Boolean,
  },

  computed:{
    classes(){
      const classes = [
        'flex', 
        'flex-col', 
        'items-center', 
        'px-6', 
        'py-5', 
        'hover:bg-gray-100',
      ]

      return this.isActive ? [...classes, 'text-red-500'] : classes
    }
  }
}
</script>