<template>
  <input
    type="text"
    placeholder="Search"
    :class="classes"
  />
</template>


<script>
export default{
  data(){
    return{
      classes:[
        'w-full', 
        'px-3', 
        'shadow-inner', 
        'rounded-bl-sm', 
        'rounded-tl-sm', 
        'border', 
        'border-gray-300', 
        'focus:outline-none', 
        'focus:border-blue-700'
      ]
    }
  },

  mounted(){
    if(window.innerWidth < 640){
      this.$el.focus()
    }
  }
}
</script>
