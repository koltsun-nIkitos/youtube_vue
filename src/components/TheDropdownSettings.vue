<template>
  <div
    class="opacity-0 group-hover:opacity-100 absolute top-9 -right-full sm:right-0 bg-white w-72 border border-t-0"
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

        <!-- <DropdownSettingsListItem  label="Apperance: Light" with-sub-menu/>
        <DropdownSettingsListItem  label="Language: English" with-sub-menu/>
        <DropdownSettingsListItem  label="Location: Russia" with-sub-menu/>
        <DropdownSettingsListItem  label="Settings"/>
        <DropdownSettingsListItem  label="You data in YouTube"/>
        <DropdownSettingsListItem  label="Help"/>
        <DropdownSettingsListItem  label="Send feedback"/>
        <DropdownSettingsListItem label="Keyboard shortcuts"/> -->
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
}
</script>