<template>
<div id="bool">
  
  <h2>Use HTML</h2>
  
  <template v-if="templateShow">
    <div class="templateShow">
      <button @click="show = !show">表示Toggle</button>  
      <div v-if="show">表示トグル</div>
      <div v-if="(new Date).getHours() < 12">午前</div>
      <div v-else-if="(new Date).getHours() >= 12 && (new Date).getHours() <= 16">午後</div>
      <div v-else-if="(new Date).getHours() >= 17">Night</div> 
    </div>  
  </template> 
<button @click="templateShow = !templateShow">templateShow </button>
  
  <h2>Use Method</h2>
  <p v-if="getTime() == 'pm' ">PM</p>
  <p v-else-if="getTime() == 'night' ">Night</p> 
</div>
</template>

<script>
export default{
  data() {
    return {
      show: false,
      templateShow: true,
      time: (new Date()).getHours()
    }
  },
  methods: {
    getTime(){
      if(this.time > 12 && this.time < 18){
        return 'pm'
      } else if(this.time >= 18){
        return 'night'
      }
    }
  }
}
</script> 

<style scoped lang="css">
#bool{
  padding: 40px;
}
.templateShow{
  border: 1px solid #ccc;
  padding: 20px;
  margin: 12px;
}
</style>