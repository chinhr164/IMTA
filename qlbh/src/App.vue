<template>
  <Products />
  <About />
  <Footer />
</template>

<script>
import Products from "./components/Products.vue";
import About from "./components/AboutUs.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Products,
    About,
    Footer,
  },
};
</script>
