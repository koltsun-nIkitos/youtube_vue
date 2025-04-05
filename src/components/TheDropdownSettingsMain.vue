<template>
  <section class="py-2 border-b">
    <ul>
      <DropdownSettingsListItem
        v-for="listItem in listItems.slice(0, 8)"
        :key="listItem.label"
        :icon="listItem.icon"
        :label="listItem.label"
        :with-sub-menu="listItem.withSubMenu"
        @click.stop="$emit('select-menu', 'appearance')"
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
</template>



<script>
import DropdownSettingsListItem from './DropdownSettingsListItem.vue';

export default{
  components:{
    DropdownSettingsListItem,
  },

  emits: ['select-menu'],

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