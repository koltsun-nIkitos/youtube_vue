<template>
  <div class="relative">
    <BaseTooltip text="Settings">
      <button @click="toggle()" class="relative  p-2 focus-outline-none">
        <BaseIcon name="dotsVertical" class="w-5 h-5"/>
      </button>
    </BaseTooltip>

    

    <!-- Выпадающий список -->
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
        @keydown.esc="close" 
        tabindex="-1"
        :class="dropdownClasses"
      >
        <TheDropdownSettingsMain 
          v-if="selectedMenu === 'main'"
          @select-menu="showSelectedMenu"
        />
        
        <TheDropdownSettingsAppearance 
          v-if="selectedMenu === 'appearance'"
          @select-menu="showSelectedMenu"
        />
      </div>
    </transition>
  </div>

  
</template>


<script>
import BaseIcon from './BaseIcon.vue';
import BaseTooltip from './BaseTooltip.vue';
import TheDropdownSettingsMain from './TheDropdownSettingsMain.vue';
import TheDropdownSettingsAppearance from './TheDropdownSettingsAppearance.vue';


export default{
  components:{
    BaseIcon,
    BaseTooltip,
    TheDropdownSettingsMain,
    TheDropdownSettingsAppearance
  },

  data() {
    return {
      isOpen : false,
      selectedMenu: 'main',
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
        this.close()
      }
    })
  },

  computed:{
    dropdownClasses(){
      return[
        'absolute', 
        'top-9', 
        '-right-full', 
        'sm:right-0', 
        'bg-white', 
        'w-72', 
        'border', 
        'border-t-0', 
        'focus:outline-none',
      ]
    }
  },

  methods:{
    showSelectedMenu(selectedMenu){
      this.selectedMenu = selectedMenu 
      this.$refs.dropdown.focus()
    },

    close(){
      this.isOpen = false

      setTimeout(() => this.selectedMenu = 'main', 200)// appearance
    },

    open(){
      this.isOpen = true
    },

    toggle(){
      this.isOpen  ? this.close() : this.open()
    }
  }
}
</script>