<template>
  <section class="flex border-b border-gray-200 text-black">
    <button @click.stop="$emit('select-menu', 'main')" class="px-3 focus:outline-none">
      <BaseIcon name="arrowLeft" />
    </button>

    <span class="py-3">Apperance</span>
  </section>
  <section class="py-2">
    <div class="text-gray-500 text-xs p-3">Settings applies to this browser only</div>
    <ul>
      <DropdownSettingsListItem
        v-for="theme, themeId in themes"
        :key="themeId"
        :label="theme"
        :active="themeId === selectedThemeId"
        @click="selectedThemeId = themeId"
      />
    </ul>
  </section>

  
</template>



<script>
import DropdownSettingsListItem from './DropdownSettingsListItem.vue';
import BaseIcon from './BaseIcon.vue';

export default{
  components:{
    DropdownSettingsListItem,
    BaseIcon
  },

  data() {
    return {
      selectedThemeId: 0,
      themes: [
        "Use device theme",
        "Dark theme",
        "Light theme",
      ]
    }
  },

  
}
</script>