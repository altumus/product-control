<template>
  <div class="fixed p-[16px] top-0 left-0 right-0 h-screen w-[300px] bg-[#393E46]">
    <UserTab />
    <div class="mt-[30px]">
      <MenuTab
        v-for="(tab, idx) in tabsRoutes"
        :key="idx"
        class="my-[20px]"
        :name="tab.name"
      />
    </div>
  </div>
</template>
<script>
import UserTab from '@/components/AsideMenuComponents/UserTab.vue'
import MenuTab from '@/components/AsideMenuComponents/MenuTab'

export default {
    components: {
      UserTab,
      MenuTab
  },
  data () {
    return {
      tabsRoutes: [
        { name: 'Товары' },
        { name: 'Продажи' },
        { name: 'Сотрудники' }
      ]
    }
  }
}
</script>