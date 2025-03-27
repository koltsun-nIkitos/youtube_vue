<template>
  <aside
    class="no-scrollbar hidden xl:block w-64 max-h-screen overflow-auto fixed top-0 pt-12 bg-white z-20"
  >
    <SidebarSection>
      <ul>
        <SidebarItem label="Home" icon="home" isActive/>
        <SidebarItem label="Trending" icon="fire" />
        <SidebarItem label="Subscriptions" icon="collection" />
      </ul>
    </SidebarSection>
    
    <SidebarSection>
      <ul>
        <SidebarItem label="Library" icon="duplicate" />
        <SidebarItem label="History" icon="clock" />
      </ul>
    </SidebarSection>

    <SidebarSection class="px-8 py-4 border-b font-medium leading-5">
      <span class="text-sm">
        Sign in to like videos, comment, and subscribe
      </span>
      <ButtonLogin class="focus:outline-none flex items-center px-2 py-0.5 mt-3 text-sm text-blue-700 uppercase border border-blue-700 rounded-sm"/>
    </SidebarSection>

    <SidebarSection>
      <SidebarSectionHeading title="best of YouTube"/>
      
      <ul>
        <SidebarItem label="Music" icon="musicNote"/>
        <SidebarItem label="Sports" icon="speakerphone"/>
        <SidebarItem label="Gaming" icon="puzzle"/>
        <SidebarItem label="Movies" icon="film"/>
        <SidebarItem label="News" icon="newspaper"/>
        <SidebarItem label="Live" icon="statusOnline"/>
        <SidebarItem label="360&deg; Video" icon="eye"/>
      </ul>
    </SidebarSection>

    <SidebarSection>
      <ul>
        <SidebarItem label="Browse channels" icon="plusCircle"/>
      </ul>
    </SidebarSection>

    <SidebarSection>
      <sidebarSectionHeading title="more from youtube" />
        
      <ul>
        <SidebarItem label="YouTube Premium" icon="play"/>
        <SidebarItem label="Live" icon="statusOnline"/>
      </ul>
    </SidebarSection>

    <SidebarSection>
      <ul>
        <SidebarItem label="Settings" icon="cog"/>
        <SidebarItem label="Report history" icon="flag"/>
        <SidebarItem label="Help" icon="questionMarkCircle"/>
        <SidebarItem label="Send feedback" icon="annotation"/>
      </ul>
    </SidebarSection>

    <SidebarSection class="px-6 py-4 text-xs font-semibold space-y-4">
      <TheFooter />
      
    </SidebarSection>

  </aside>
</template>


<script>
import SidebarSection from './SidebarSection.vue';
import SidebarSectionHeading from './SidebarSectionHeading.vue';
import SidebarItem from './SidebarItem.vue';
import ButtonLogin from './ButtonLogin.vue';
import TheFooter from './TheFooter.vue';

export default{
  components: {
    SidebarSection,
    SidebarSectionHeading,
    SidebarItem,
    ButtonLogin,
    TheFooter,

  }
}
</script>