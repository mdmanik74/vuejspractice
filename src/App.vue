<template>
  <div id="app">
<navbar></navbar>
<div class="containers">
<div class="row">
  <div class="col-sm-9">
     
   <product @newItemAdded="addCartItem" :items="items"></product>  
   </div>
   <div class="col-sm-3">
   <cart @itemRemoved="removeItem" :items="cart"></cart>
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
   items: [],
   cart:[]
 }
  },
  mounted(){
   this.items=data
  },
  methods:{
    addCartItem(item){
      this.cart.push(item)
    },
    removeItem(index){
      this.cart.splice(index,1)
    }
  }
}
</script>

<style>
.containers{
padding:20px;
}
</style>