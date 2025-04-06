<template>
  <section class="py-2 border-b">
    <ul>
      <DropdownSettingsListItem
        v-for="listItem in listItems.slice(0, 8)"
        :key="listItem.label"
        :icon="listItem.icon"
        :label="listItem.label"
        :with-sub-menu="listItem.withSubMenu"
        @click.stop="selectMenu(listItem)"
        />
    </ul>
  </section>

  <section class="py-2">
    <ul>
      <DropdownSettingsListItem
        :label="listItems[8].label"
        :icon="listItems[8].icon"
        :with-sub-menu="listItems[8].withSubMenu"
        @click.stop="selectMenu(listItems[8])"
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
          id: 'appearance',
          icon:"sun",
          label:"Appearance: Light",
          withSubMenu:true,
        },
        {
          id: 'language',
          icon:"translate",
          label:"Language: English",
          withSubMenu:true,
        },
        {
          id: 'location',
          icon:"globeAlt",
          label:"Location: Russia",
          withSubMenu:true,
        },
        {
          id: 'settings',
          icon:"cog",
          label:"Settings",
          withSubMenu:false,
        },
        {
          id: 'you_data_in_youtube',
          icon:"shieldCheck",
          label:"You data in YouTube",
          withSubMenu:false,
        },
        {
          id: 'help',
          icon:"questionMarkCircle",
          label:"Help",
          withSubMenu:false,
        },
        {
          id: 'send_feedback',
          icon:"chatAlt",
          label:"Send feedback",
          withSubMenu:false,
        },
        {
          id: 'keyboard_shortcuts',
          icon:"calculator",
          label:"Keyboard shortcuts",
          withSubMenu:false,
        },
        {
          id: 'restricted_mode',
          icon: null,
          label: "Restricted mode: Off",
          withSubMenu: true,
        },
      ]
    }
  },

  methods:{
    selectMenu(listItem){
      if(listItem.withSubMenu){
        this.$emit('select-menu', listItem.id)
      }

    }
  }
}
</script>