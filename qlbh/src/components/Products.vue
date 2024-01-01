<template>
  <div class="container">
    <div class="row">
      <div class="col" v-for="product in products" :key="product.id">
        <ItemProd
          :name="product.name"
          :price="product.price"
          :thumb="product.thumb"
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
      products: [
        {
          thumb: "../assets/itemsp.jpg",
          name: "Natural Plants",
          price: 1200,
        },
        {
          thumb: "../assets/itemsp.jpg",
          name: "Artificial Plants",
          price: 1600,
        },
        {
          thumb: "../assets/itemsp.jpg",
          name: "Artificial Plants",
          price: 900,
        },
      ],
    };
  },
};
</script>

<style scoped></style>
