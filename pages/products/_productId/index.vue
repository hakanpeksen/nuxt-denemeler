<template>
  <div>
    <p>Ürün ID Bilgisi : {{ $route.params.productId }}</p>
    <div class="button-container">
      <n-link to="/products" tag="a" class="button--green">Geri Dön</n-link>
      <button class="button--green" @click="editProduct">Düzenle</button>
    </div>
  </div>
</template>

<script>
export default {
  validate(arg) {
    console.log(arg)
    // return arg.params.productId == 2;
    return /^\d+$/.test(arg.params.productId)
  },
  methods: {
    editProduct() {
      this.$router.push('/products/' + this.$route.params.productId + '/edit')
    }
  }
}
</script>

<style scoped></style>
