<template>
  <div v-if="product">
    <div class="row">
      <div class="col-sm-2-12 product">
        <div class="card">
          <div class="card-body">
            <div class="product-image">
              <img :src="image" />
            </div>
            <h3 class="card-title">{{title}}</h3>
            <p v-if="inStock" class="card-text">em estoque</p>
            <p v-else class="card-text">sem estoque</p>
            <ul>
              <li v-for="detail in details" :key="detail">{{detail}}</li>
            </ul>
            <div
              v-for="(variant, index) in variante"
              :key="variant.variantId"
              class="color-box"
              :style="{backgroundColor: variant.variantColor}"
              @mouseover="updateProduct(index)"
            ></div>
            <div class="cart">
              <button v-on:click="addToCart" class="btn btn-primary">Add Carrinho</button>
              <p>Carrinho: {{cart}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Product",
  data() {
    return {
      cart: 0,
      brand: "Vue Mastery",
      // image: "/img/green.png",
      variante: [
        {
          variantId: 2234,
          variantColor: "green",
          variantImage: "/img/green.png"
        },
        {
          variantId: 2235,
          variantColor: "blue",
          variantImage: "/img/blue.png"
        }
      ]
    };
  },
  props: {
    product: String,
    product_image: String,
    inStock: Boolean,
    inventory: Number,
    details: Array,
    variants: Array
    // cart: Number
  },
  methods: {
    addToCart() {
      this.cart += 1;
    },
    updateProduct: function(index) {
      this.selectedVariant = index;
      console.log(index);
    }
  },
  computed: {
    title() {
      return this.brand + " " + this.product;
    },
    image() {
      return this.variante[this.selectedVariant].variantImage;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #42b983;
}
img {
  width: 300px;
  height: 300px;
}
.product {
  margin: 0, 15 px;
  padding: 0, 15 px;
}
.color-box {
  width: 40px;
  height: 40px;
  margin: 5px 0;
}
</style>
