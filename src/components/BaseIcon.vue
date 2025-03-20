<template>
  <svg
    :class="$attrs.class || 'w-6 h-6'"
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    :viewBox="$attrs.viewBox || '0 0 24 24'"
    stroke-width="1.5"
    stroke="currentColor"
    v-html="path"
    
  >
    
  </svg>
</template>

<script>
import icons from '../icons';

export default{
  props: ['name'],

  data() {
    return {
      path: icons[this.name]
    }
  },
}
</script>
