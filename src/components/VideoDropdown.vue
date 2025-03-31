<template>
  <div class="relative ml-auto -mt-1">
    <button
      @click="isOpen = !isOpen"
      class="ml-auto -mt-1 p-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
    >
      <BaseIcon class="w-6 h-6" name="dotsVertical" />
      
      <transition
        enter-active-class="transition ease-out duration-100"
        enter-from-class="transition opacity-0 scale-95"
        enter-to-class="transform opacity-100 scale-100"
        leave-active-class="transition ease-in duraton-75"
        leave-from-class="transform opacity-100 scale-100"
        leave-to-class="transform opacity-0 scale-95"
      >
        <div
            v-show="isOpen"
            ref="dropdown"
            @keydown.esc="isOpen = false" 
            tabindex="-1"
            class="absolute top-9 -right-full sm:right-0 bg-white w-48 rounded shadow focus:outline-none"
          >
            <section class="py-2">
              <ul>
                <VideoDropdownListItem 
                  icon="menuAlt3" 
                  label="Add to queque" 
                />
              </ul>
            </section>
        </div>
      </transition>
      
    </button>
  </div>
  
</template>

<script>
import BaseIcon from "./BaseIcon.vue";
import VideoDropdownListItem from "./VideoDropdownListItem.vue";

export default {
  components: {
    BaseIcon,
    VideoDropdownListItem
  },

  data() {
    return {
      isOpen : false,
    }
  },

  watch:{
    isOpen(){
      this.$nextTick(() =>{
        if(this.isOpen){
          this.$refs.dropdown.focus()
        }
      });
    }
  },

  mounted(){
    window.addEventListener('click', event =>{
      if (!this.$el.contains(event.target)){
        this.isOpen = false
      }
    })
  },
};
</script>
