<template>
  <div id="app">
<navbar></navbar>
<div class="container">
<div class="row">
  <div class="col-sm-10">
      <div class="row">
   <product></product> 

</div> 
   </div>
   <div class="col-sm-2">
   <cart></cart>
    </div>
  </div>
  </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Product from './components/Product.vue'
import Cart from './components/Cart.vue'


export default {
   components: {
    Navbar,
    Cart,
    Product
  }
}
</script>

<style>
.container{
padding:10px;
}
</style>