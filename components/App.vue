<template>
  <div id="app" class="container">
    <div class="row header-wrapper">
      <h4 class="header col s8">Shopping Cart Example</h4>
      <!-- prop example: override default free-shipping-rule value [set in Total.vue]-->
      <total class="col s4 right-align" title="Total" :free-shipping-rule="3"></total>
    </div>
    <div class="divider"></div>
    <div class="section">
      <product-list title="Products"></product-list>
    </div>
    <div class="divider"></div>
    <div class="section">
      <!-- prop example: set allow-remove to true [set in Cart.vue]-->
      <cart title="Your Cart" allow-remove></cart>
    </div>
  </div>
</template>

<script>
// Step 2: Bring in Vue components (vue layer listening to the store)
import ProductList from './ProductList.vue'
import Cart from './Cart.vue'
import Total from './Total.vue'

export default {
  components: { ProductList, Cart, Total},
  created() {
    console.log('Step 2: Bring in Vue components (vue layer listening to the store)')
  }
}
</script>
