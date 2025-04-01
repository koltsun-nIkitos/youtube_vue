<template>
  <div class="relative ml-auto -mt-1">
    <button
      @click="toggle"
      :class="buttonClasses"
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
            :class="dropDownClasses"
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
import { ref } from "vue";
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
      positionClasses: []
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

  computed:{
    buttonClasses(){
      return [
        'ml-auto', 
        '-mt-1', 
        'p-1', 
        'opacity-0', 
        'group-hover:opacity-100', 
        'text-gray-500', 
        'hover:text-gray-700', 
        'focus:outline-none',
      ]
    },

    dropDownClasses(){
      return[
        'z-10',
        'absolute', 
        // 'top-9', 
        // '-right-full', 
        // 'sm:right-0', 
        'bg-white', 
        'w-48', 
        'rounded', 
        'shadow', 
        'focus:outline-none',
        ...this.positionClasses,
      ]
    }
  },

  methods:{
    toggle(event){
      this.isOpen = !this.isOpen

      if(this.isOpen){
        this.$nextTick(() =>{
          this.positionClasses = this.getPositionClasses(event)
        })
      }
    },

    getPositionClasses(event){
      return [
        this.getTopClass(event),
        this.getRightClass(event),
        this.getLeftClass(event),
      ]
    },

    getTopClass(event){
      const clickCoordY = event.clientY
      const buttonHeight = event.currentTarget.offsetHeight
      const dropdownHeight = this.$refs.dropdown.offsetHeight

      if (window.innerHeight - clickCoordY < dropdownHeight){
        return '-top-14'
      }

      if (window.innerHeight - clickCoordY < dropdownHeight + buttonHeight){
        return 'top-0'
      }

      return 'top-9'
    },

    getRightClass(event){
      const clickCoordX = event.clientX
      const clickCoordY = event.clientY
      const buttonHeight = event.currentTarget.offsetHeight
      const dropdownWidth = this.$refs.dropdown.offsetWidth
      const dropdownHeight = this.$refs.dropdown.offsetHeight

      if (window.innerWidth - clickCoordX > dropdownWidth){
        return 'right-auto'
      }

      if (window.innerHeight - clickCoordY > dropdownHeight + buttonHeight){
        return 'right-0'
      }

      if(window.innerHeight - clickCoordY > dropdownHeight){
        return 'right-8'
      }

      return 'right-0'
    },

    getLeftClass(event){
      const clickCoordX = event.clientX
      const clickCoordY = event.clientY
      const buttonHeight = event.currentTarget.offsetHeight
      const dropdownWidth = this.$refs.dropdown.offsetWidth
      const dropdownHeight = this.$refs.dropdown.offsetHeight

      if (window.innerWidth - clickCoordX < dropdownWidth){
        return 'right-auto'
      }

      if (window.innerHeight - clickCoordY < dropdownHeight){
        return 'left-auto'
      }

      if(window.innerHeight - clickCoordY > dropdownHeight + buttonHeight){
        return ' left-auto'
      }

      return 'left-8'
    },
  },
};
</script>
