<template>
  <div class="w-[calc(100%-300px)] p-[30px] ml-[300px] flex content-start flex-wrap h-screen bg-[#EEEEEE]">
    <template
      v-for="(product, idx) in products"
      :key="idx"
    >
      <div class="w-[350px] bg-[#F9F7F7] rounded border-[#00ADB5] border-[1px] h-[60px] mb-[20px] mr-[10px]">
        <div class="flex flex-col p-[5px]">
          <input
            class="font-bold text-[16px] bg-[#F9F7F7] focus:outline-none"
            :value="product.name"
            @blur="showMessage"
          >
          <span class="text-[15px] text-[#7E7E80]">Кол-во товара: {{ product.amount }}</span>
        </div>
      </div>
    </template>
  </div>
</template>
<script>
export default {
  computed: {
    products () {
      return this.$store.state.products.products
    }
  },
  methods: {
    showMessage (e) {
      alert(`Теперь этот продукт называется - ${e.target.value} !`)
    }
  }
}
</script>
