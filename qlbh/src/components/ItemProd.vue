<template>
  <div class="product-item">
    <img src="`${{thumb}}`" alt="Product Image" class="product-image" />
    <h4 class="name-item">{{ name }}</h4>
    <p class="price-item">{{ price }}</p>
    <button class="btn btn-primary btn-add-to-cart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: "ItemProd",
  props: {
    name: {
      type: String,
      required: true,
    },
    price: {
      type: Number,
      required: true,
    },
    thumb: {
      type: String,
      required: false,
    },
  },
};
</script>

<style scoped>
.product-item {
  height: 436px;
  width: 250px;
  margin: 10px;
  text-align: left;
}
.name-item {
  font-size: 18px;
  line-height: 27px;
  font-weight: 600;
  font-family: "Arial";
}
.price-item {
  font-size: 18px;
  line-height: 27px;
  color: grey;
}

.product-image {
  max-height: 363px;
  max-width: 100%;
  margin-bottom: 10px;
}

.btn-add-to-cart {
  width: 100%;
  background-color: #c1dcdc;
  border: #c1dcdc;
}
</style>
