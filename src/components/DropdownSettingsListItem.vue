<template>
  <li>
    <a href="#" class="flex items-center px-4 py-2 text-sm hover:bg-gray-100">
      <BaseIcon 
        v-if="isIconShown" 
        :name="iconName" 
        class="w-5 h-5 mr-3 text-gray-400" 
      />

      <span :class="{ 'ml-8' : !isIconShown }">{{ label }}</span>

      <BaseIcon v-if="withSubMenu" name="chevronRight" class="w-5 h-5 text-gray-400 ml-auto" />

    </a>
  </li>
</template>


<script>
import BaseIcon from './BaseIcon.vue';

export default{
  components:{
    BaseIcon,
  },

  props:{
    active: Boolean,
    icon: {
      type: String,
      default: 'check'
    },
    'label':String,
    'withSubMenu':Boolean
  },

  computed:{
    isIconShown(){
      return this.active || this.icon !== 'check'
    },

    iconName(){
      return this.active ? 'check' : this.icon
    }
  }

}
</script>
