<template>
  <div>
    <input v-model="productID" type="text" />
    <button class="button--green" @click="showProduct">Ürünü Göster</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      productID: null
    }
  },
  methods: {
    showProduct() {
      this.$router.push('/products/' + this.productID)
    }
  }
}
</script>

<style scoped></style>
