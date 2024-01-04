<template>
  <div class="container">
    <div class="row">
      <div class="col" v-for="product in products" :key="product.id">
        <ItemProd
          :name="product.name"
          :price="product.price"
          :img="product.img"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ItemProd from "./ItemProd.vue";
export default {
  name: "Products_",
  components: {
    ItemProd,
  },
  data() {
    return {
      products: [],
    };
  },
  created() {
    fetch("https://65937a4abb1297071990a088.mockapi.io/products/product_item")
      .then((response) => response.json())
      .then((data) => (this.products = data));
  },
};
</script>

<style scoped></style>
