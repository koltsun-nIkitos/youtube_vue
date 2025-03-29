<template>
  <div class="relative">
    <button @click="isOpen = !isOpen" class="relative  p-2 focus-outline-none">
        <BaseIcon name="dotsVertical" class="w-5 h-5"/>
    </button>

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
        class="absolute top-9 -right-full sm:right-0 bg-white w-72 border border-t-0"
      >
        <section class="py-2 border-b">
          <ul>
            <DropdownSettingsListItem 
              v-for="listItem in listItems.slice(0, 8)"
              :key="listItem.label"
              :icon="listItem.icon" 
              :label="listItem.label" 
              :with-sub-menu="listItem.withSubMenu"
            />

          </ul>
        </section>

        <section class="py-2">
          <ul>
            <DropdownSettingsListItem  
              :label="listItems[8].label" 
              :with-sub-menu="listItems[8].withSubMenu"
            />
          </ul>
        </section>
      </div>
    </transition>
  </div>

  
</template>


<script>
import BaseIcon from './BaseIcon.vue';
import DropdownSettingsListItem from './DropdownSettingsListItem.vue';

export default{
  components:{
    BaseIcon,
    DropdownSettingsListItem
  },

  data() {
    return {
      isOpen : false,

      listItems: [
        {
          icon:"sun",
          label:"Apperance: Light",
          withSubMenu:true,
        },
        {
          icon:"translate",
          label:"Language: English",
          withSubMenu:true,
        },
        {
          icon:"globeAlt",
          label:"Location: Russia",
          withSubMenu:true,
        },
        {
          icon:"cog",
          label:"Settings",
          withSubMenu:false,
        },
        {
          icon:"shieldCheck",
          label:"You data in YouTube",
          withSubMenu:false,
        },
        {
          icon:"questionMarkCircle",
          label:"Help",
          withSubMenu:false,
        },
        {
          icon:"chatAlt",
          label:"Send feedback",
          withSubMenu:false,
        },
        {
          icon:"calculator",
          label:"Keyboard shortcuts",
          withSubMenu:false,
        },
        {
          icon: null,
          label: "Restricted mode: Off",
          withSubMenu: true,
        },
      ]
    }
  },

  mounted(){
    window.addEventListener('click', event =>{
      if (!this.$el.contains(event.target)){
        this.isOpen = false
      }
    })
  },
}
</script>