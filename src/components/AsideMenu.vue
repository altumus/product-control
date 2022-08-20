<template>
  <div class="fixed top-0 left-0 right-0 h-screen w-[300px] bg-[#355E3B]">
    <UserTab />
    <div class="mt-[30px]">
      <MenuTab
        v-for="i in 5"
        :key="i"
        class="my-[10px]"
        :name="`Какое-то имя под номером ${i}`"
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
}
}
</script>