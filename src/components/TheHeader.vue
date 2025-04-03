<template>
  <header :class="classes">
    <div
      :class="[
        'lg:w-1/4',
        'flex',
        isMobileSearchShown ? 'opacity-0' : 'opacity-100',
      ]"
    >
      <div class="flex items-center xl:w-64 xl:bg-white pl-4">
        <button
          @click="$emit('toggleSidebar')"
          class="mr-3 sm:ml-2 sm:mr-6 focus:outline-none"
        >
          <BaseIcon name="menu" />
        </button>

        <LogoMain />
      </div>
    </div>

    <TheSearchMobile v-if="isMobileSearchShown" @close="closeMobileSearch" />

    <div
      v-else
      class="hidden sm:flex p-2.5 flex items-center justify-end pl-8 md:pl-12 md:px-8 lg:px-0 flex-1 lg:w-1/2 max-w-screen-md"
    >
      <TheSearch />

      <BaseTooltip text="Search with your voice">
        <button class="p-2 focus:outline-none">
          <BaseIcon name="microphone" class="w-5 h-5 text-black-700" />
        </button>
      </BaseTooltip>
    </div>

    <div
      :class="[
        'flex',
        'items-center',
        'justify-end',
        'sm:space-x-3',
        'lg:w-1/4',
        'p-2',
        'sm:px-4',
        isMobileSearchShown ? 'opacity-0' : 'opacity-100'
      ]"
    >
      <BaseTooltip text="Search with your voice">
        <button class="sm:hidden focus:outline-none">
          <BaseIcon name="microphone" class="w-5 h-5" />
        </button>
      </BaseTooltip>

      <BaseTooltip text="Search">
        <button
          @click.stop="isMobileSearchActive = true"
          class="sm:hidden p-2 focus:outline-none"
        >
          <BaseIcon name="search" class="w-5 h-5" />
        </button>
      </BaseTooltip>

      <!-- Выпадающий список -->
      <TheDropdownApps />

      <!-- Выпадающий список -->
      <TheDropdownSettings />

      <ButtonLogin />
    </div>
  </header>
</template>

<script>
import TheSearchMobile from "./TheSearchMobile.vue";
import TheDropdownApps from "./TheDropdownApps.vue";
import TheDropdownSettings from "./TheDropdownSettings.vue";
import LogoMain from "./LogoMain.vue";
import TheSearch from "./TheSearch.vue";
import ButtonLogin from "./ButtonLogin.vue";
import BaseIcon from "./BaseIcon.vue";
import BaseTooltip from "./BaseTooltip.vue";

export default {
  components: {
    BaseIcon,
    LogoMain,
    TheSearch,
    TheSearchMobile,
    TheDropdownApps,
    TheDropdownSettings,
    ButtonLogin,
    BaseTooltip,
  },

  emits: {
    toggleSidebar: null,
  },

  data() {
    return {
      isSmallScreen: false,
      isMobileSearchActive: false,
      classes: [
        "flex",
        "bg-white",
        "justify-between",
        "bg-opacity-95",
        "w-full",
      ],
    };
  },

  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize);
  },

  methods: {
    onResize() {
      if (window.innerWidth < 648) {
        this.isSmallScreen = true;
        return;
      }

      this.closeMobileSearch();
      this.isSmallScreen = false;
    },

    closeMobileSearch() {
      this.isMobileSearchActive = false;
    },
  },

  computed: {
    isMobileSearchShown() {
      return this.isSmallScreen && this.isMobileSearchActive;
    },
  },
};
</script>
