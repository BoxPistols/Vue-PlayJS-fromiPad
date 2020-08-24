<template>
<div id="bool">
  <button @click="show = !show">表示Toggle</button>
  <div v-if="show">表示トグル</div>
  <div v-if="(new Date).getHours() < 12">午前</div>
  <div v-else-if="(new Date).getHours() >= 12 && (new Date).getHours() <= 16">午後</div>
  <div v-else-if="(new Date).getHours() >= 17">Night</div>
</div>
</template>

<script>
export default{
  data() {
    return {
      show: false
    }
  }
}
</script> 

<style scoped lang="css">
#bool{
  padding: 40px;
}
</style>