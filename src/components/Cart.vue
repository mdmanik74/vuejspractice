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
      <button @click="removeItem(index)" type="button" class="btn btn-danger"> <span class="glyphicon glyphicon-trash"></span> Trash </button>
    </tr>
   
  </tbody>
  <tr>
      <th scope="col">Total</th>
      <th scope="col">{{ total }}</th>
      <th scope="col"></th>
    </tr>
</table>
</template>
<script>

export default {
   props:['items'],
   computed:{
	   total(){
		   var total =0
		   this.items.forEach(item => {
			   total+= parseFloat(item.price)
			   })
			   return total
		   }
   },
   methods:{
     removeItem(index){
       this.$emit('itemRemoved',index)
     }
   }
}
</script>
<style lang="stylus" scoped>

</style>