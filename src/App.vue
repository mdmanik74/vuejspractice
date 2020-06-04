<template>
  <div id="app">
<navbar></navbar>
<div class="container">
<div class="row">
  <div class="col-sm-10">
     
   <product :items="items"></product>  
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
import data from './data.js'


export default {
   components: {
    Navbar,
    Cart,
    Product
  },
  data(){
 return{
   items: []
 }
  },
  mounted(){
   this.items=data
  }
}
</script>

<style>
.container{
padding:10px;
}
</style>