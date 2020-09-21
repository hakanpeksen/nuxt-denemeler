<template>
  <div>
    <h3 class="title">Ürün Düzenleme</h3>
    <p>Ürün ID Bilgisi : {{ $route.params.productId }}</p>
    <div class="button-container">
      <n-link
        :to="'/products/' + $route.params.productId"
        tag="a"
        class="button--green"
        >Geri Dön</n-link
      >
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped></style>
