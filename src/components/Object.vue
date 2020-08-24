<template>
<div class="obj">
  
  <h2>Component</h2>  
  
  <ul v-for="(c, i) in hasJiro" key="id">
    <li>{{ i }} {{ c.name }}</li>
  </ul>
  
  <hr>
  
  <ul v-for="(c, i) in overOne" key="id">
    <li>{{ i }}: {{ c.id }} / {{ c.name }}</li>
  </ul>
  
  <hr>
  
<!--  <ul>
    <li v-for="v, k in customers">{{ k }} {{ v }}</li>
  </ul>
-->
  
</div>
</template>

<script>
let cs = 
  [
    {id: 1, name: '大竹真琴', age: 20},
    {id: 2, name: '大竹次郎', age: 30},
    {id: 3, name: '大竹三郎', age: 40},         
  ]

export default{
  data() {
    return {
      customers: cs
   }
  },
  computed:{
    hasJiro(){
      return this.customers.filter(function(e){
        return e.name == "大竹次郎"
      })
    },
    overOne(){
      return this.customers.filter(function(e){
        return (e.age >= 40)
      })
    },
  }
}

</script>

<style>
.obj{
 }
</style>