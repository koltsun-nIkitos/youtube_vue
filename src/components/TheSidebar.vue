<template>
  <aside
    class="no-scrollbar hidden xl:block w-64 max-h-screen overflow-auto fixed top-0 pt-12 bg-white z-20"
  >
    <section class="py-2 border-b">
      <ul>
        <SidebarItem label="Home" icon="home" isActive/>
        <SidebarItem label="Trending" icon="fire" />
        <SidebarItem label="Subscriptions" icon="collection" />
      </ul>
    </section>

    <section class="py-2 border-b">
      <ul>
        <SidebarItem label="Library" icon="duplicate" />
        <SidebarItem label="History" icon="clock" />
      </ul>
    </section>

    <section class="px-8 py-4 border-b font-medium leading-5">
      <span class="text-sm"
        >Sign in to like videos, comment, and subscribe</span
      >

      <button
        class="focus:outline-none flex items-center px-2 py-0.5 mt-3 text-sm text-blue-700 uppercase border border-blue-700 rounded-sm"
      >
        <svg
          class="mr-2 w-7 h-7"
          width="800px"
          height="800px"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            fill="rgb(29,78,216)"
            clip-rule="evenodd"
            d="M22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12ZM15 9C15 10.6569 13.6569 12 12 12C10.3431 12 9 10.6569 9 9C9 7.34315 10.3431 6 12 6C13.6569 6 15 7.34315 15 9ZM12 20.5C13.784 20.5 15.4397 19.9504 16.8069 19.0112C17.4108 18.5964 17.6688 17.8062 17.3178 17.1632C16.59 15.8303 15.0902 15 11.9999 15C8.90969 15 7.40997 15.8302 6.68214 17.1632C6.33105 17.8062 6.5891 18.5963 7.19296 19.0111C8.56018 19.9503 10.2159 20.5 12 20.5Z"
          />
        </svg>
        Sign In
      </button>
    </section>

    <section class="py-2 border-b">
      <div class="uppercase text-sm font-semibold px-6 py-2">
        best of YouTube
      </div>
      <ul>
        <SidebarItem label="Music" icon="musicNote"/>
        <SidebarItem label="Sports" icon="speakerphone"/>
        <SidebarItem label="Gaming" icon="puzzle"/>
        <SidebarItem label="Movies" icon="film"/>
        <SidebarItem label="News" icon="newspaper"/>
        <SidebarItem label="Live" icon="statusOnline"/>
        <SidebarItem label="360&deg; Video" icon="eye"/>
      </ul>
    </section>

    <section class="py-2 border-b">
      <ul>
        <SidebarItem label="Browse channels" icon="plusCircle"/>
      </ul>
    </section>

    <section class="py-2 border-b">
      <div class="uppercase text-sm font-semibold px-6 py-2">
        more from youtube
      </div>
      <ul>
        <SidebarItem label="YouTube Premium" icon="play"/>
        <SidebarItem label="Live" icon="statusOnline"/>
      </ul>
    </section>

    <section class="py-2 border-b">
      <ul>
        <SidebarItem label="Settings" icon="cog"/>
        <SidebarItem label="Report history" icon="flag"/>
        <SidebarItem label="Help" icon="questionMarkCircle"/>
        <SidebarItem label="Send feedback" icon="annotation"/>
      </ul>
    </section>

    <section class="px-6 py-4 text-xs font-semibold space-y-4">
      <div>
        <a href="#" class="mr-2">About</a>
        <a href="#" class="mr-2">Press</a>
        <a href="#" class="mr-2">Copyright</a>
        <a href="#" class="mr-2">Contact us</a>
        <a href="#" class="mr-2">Creators</a>
        <a href="#" class="mr-2">Advertise</a>
        <a href="#" class="mr-2">Developers</a>
      </div>
      <div>
        <a href="#" class="mr-2">Terms</a>
        <a href="#" class="mr-2">Privacy</a>
        <a href="#" class="mr-2">Policy & Safety</a>
        <a href="#" class="mr-2">How YouTube works</a>
        <a href="#" class="mr-2">Test new features</a>
      </div>
      <div class="font-normal text-gray-500">&copy; 2025 Google LLC</div>
    </section>
  </aside>
</template>


<script>
import SidebarItem from './SidebarItem.vue';
export default{
  components: {
    SidebarItem,
  }
}
</script>