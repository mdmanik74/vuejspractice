<template>
<table class="table">
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Price</th>
      <th scope="col">Action</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(item, index) in items" :key="index">
      <td>{{ item.title }}</td>
      <td>{{ item.price }}</td>
      <td>Rem</td>
    </tr>
   <tr>
      <th scope="col">Total</th>
      <th scope="col">{{ totalPrice }}</th>
      <th scope="col"></th>
    </tr>
  </tbody>
</table>
</template>
<script>

export default {
   props:['items'],
   computed:{
	   totalPrice(){
		   var total=0
		   this.items.forEach(item=>{
			   total += parseFloat(item.price)
		   })
		   return total
	   }
   }
}
</script>
<style lang="stylus" scoped>

</style>