<template>
  <div>
    <Navbar></Navbar>
    <div class="container">
      <Product
        :product="product"
        :product_image="product_image"
        :inStock="inStock"
        :inventory="inventory"
        :details="details"
        :variants="variants"
      />
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Product from "./components/Product.vue";

export default {
  name: "app",
  data() {
    return {
      product: "Meia da boa",
      product_image: "/img/green.png",
      inStock: true,
      inventory: 88,
      cart: 0,
      details: ["80% coton", "20% Poliester", "gender neutrall"],
      variants: [
        {
          variantId: 2234,
          variantColor: "green",
          variantImage: "/img/green.png"
        },
        {
          variantId: 2235,
          variantColor: "blue",
          variantImage: "/img/rosa.png"
        }
      ]
    };
  },
  components: {
    Navbar,
    Product
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
