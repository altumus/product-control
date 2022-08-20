<template>
  <div
    class="w-full h-[40px] bg-[#DCDCDC]"
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
