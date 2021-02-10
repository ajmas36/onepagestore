<template>
  <div>
    <h1>Your Future One Page store is here</h1>
    <navbar :cart="cart" :cartQty="cartQty" :cartTotal="cartTotal"></navbar>
    <price-slider :sliderStatus="sliderStatus" :maximum.sync="maximum"></price-slider>
    <product-list :maximum="maximum" :products="products"></product-list>
  </div>
</template>
<style>
    h1 {
    color: whitesmoke;
    font-style: italic;
    font-family: fantasy;
    text-align: center;
    margin-bottom: 20px;
            text-shadow: 2px 2px chocolate;
    }
</style>
<script>
import Navbar from "./Navbar.vue";
import PriceSlider from "./PriceSlider.vue";
import ProductList from "./ProductList.vue";

export default {
  name: "products",
  props: [
    "products",
    "maximum",
    "cart",
    "cartQty",
    "cartTotal",
    "sliderStatus",
    "sliderState"
  ],
  components: {
    Navbar,
    PriceSlider,
    ProductList
  }
};
</script>
