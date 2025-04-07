<template>
  <div class="relative">
    <BaseTooltip text="Settings">
      <button @click="toggle()" class="relative p-2 focus-outline-none">
        <BaseIcon name="dotsVertical" class="w-5 h-5" />
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
        <component
          v-if="selectedMenu"
          :is="menu"
          :selected-options="selectedOptions"
          @select-option="selectOption"
          @close="closeMenu"
        />

        <TheDropdownSettingsMain
          v-else
          :menu-items="menuItems"
          @select-menu="selectMenu"
        />
      </div>
    </transition>
  </div>
</template>

<script>
import BaseIcon from "./BaseIcon.vue";
import BaseTooltip from "./BaseTooltip.vue";
import TheDropdownSettingsMain from "./TheDropdownSettingsMain.vue";
import TheDropdownSettingsAppearance from "./TheDropdownSettingsAppearance.vue";
import TheDropdownSettingsLanguage from "./TheDropdownSettingsLanguage.vue";
import TheDropdownSettingsLocation from "./TheDropdownSettingsLocation.vue";
import TheDropdownSettingsRestrictedMode from "./TheDropdownSettingsRestrictedMode.vue";

export default {
  components: {
    BaseIcon,
    BaseTooltip,
    TheDropdownSettingsMain,
    TheDropdownSettingsAppearance,
    TheDropdownSettingsLanguage,
    TheDropdownSettingsLocation,
    TheDropdownSettingsRestrictedMode,
  },

  data() {
    return {
      isOpen: false,
      selectedMenu: null,
      selectedOptions: {
        theme: {
          id: 0,
          text: "Device Theme",
        },
        language: {
          id: 0,
          text: "English",
        },
        location: {
          id: 0,
          text: "United States",
        },
        restrictedMode: {
          enabled: false,
          text: "Off",
        },
      },
    };
  },

  watch: {
    isOpen() {
      this.$nextTick(() => {
        if (this.isOpen) {
          this.$refs.dropdown.focus();
        }
      });
    },
  },

  mounted() {
    window.addEventListener("click", (event) => {
      if (!this.$el.contains(event.target)) {
        this.close();
      }
    });
  },

  computed: {
    dropdownClasses() {
      return [
        "absolute",
        "top-9",
        "-right-full",
        "sm:right-0",
        "bg-white",
        "w-72",
        "border",
        "border-t-0",
        "focus:outline-none",
      ];
    },

    menu() {
      const menuComponentNames = {
        appearance: "TheDropdownSettingsAppearance",
        language: "TheDropdownSettingsLanguage",
        location: "TheDropdownSettingsLocation",
        restricted_mode: "TheDropdownSettingsRestrictedMode",
      };

      return this.selectMenu ? menuComponentNames[this.selectedMenu.id] : null;
    },

    menuItems() {
      return [
        {
          id: "appearance",
          icon: "sun",
          label: "Appearance: " + this.selectedOptions.theme.text,
          withSubMenu: true,
        },
        {
          id: "language",
          icon: "translate",
          label: "Language: " + this.selectedOptions.language.text,
          withSubMenu: true,
        },
        {
          id: "location",
          icon: "globeAlt",
          label: "Location: " + this.selectedOptions.location.text,
          withSubMenu: true,
        },
        {
          id: "settings",
          icon: "cog",
          label: "Settings",
          withSubMenu: false,
        },
        {
          id: "you_data_in_youtube",
          icon: "shieldCheck",
          label: "You data in YouTube",
          withSubMenu: false,
        },
        {
          id: "help",
          icon: "questionMarkCircle",
          label: "Help",
          withSubMenu: false,
        },
        {
          id: "send_feedback",
          icon: "chatAlt",
          label: "Send feedback",
          withSubMenu: false,
        },
        {
          id: "keyboard_shortcuts",
          icon: "calculator",
          label: "Keyboard shortcuts",
          withSubMenu: false,
        },
        {
          id: "restricted_mode",
          icon: null,
          label: "Restricted mode: " + this.selectedOptions.restrictedMode.text,
          withSubMenu: true,
        },
      ];
    },
  },

  methods: {
    close() {
      this.isOpen = false;

      setTimeout(this.closeMenu, 200); // appearance
    },

    selectMenu(menu) {
      this.selectedMenu = menu;
      this.$refs.dropdown.focus();
    },

    closeMenu() {
      this.selectMenu(null);
    },

    open() {
      this.isOpen = true;
    },

    toggle() {
      this.isOpen ? this.close() : this.open();
    },

    selectOption(option) {
      this.selectedOptions[option.name] = option.value;
    },
  },
};
</script>
