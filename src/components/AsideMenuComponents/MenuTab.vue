<template>
  <div
    class="w-full h-[40px] bg-[#EEEEEE] rounded flex items-center justify-center hover:cursor-pointer"
  >
    <span>{{ name }}</span>
  </div>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      default: ''
    },
    linkTo: {
      type: String,
      default: ''
    }
  }
}
</script>
