<template>
  <div class="">
    <h1 :style="{color: color, fontSize: size + 'em'}">{{ msg }}</h1>
    <p>
      <span @click="ev02()">Size + </span>
      <span @click="ev03()">Size - </span> 
      <span @click="ev04(+0.2)">Size Set </span>   
    </p>
    <hr>
    <button class="btn" @click="ev01()">Button</button>
    <h2 :style="[myStyle, newStyle]">{{ kuji }}</h2>
 </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome',
      color: 'orange',
      size: 1.5,
      // Omikuji
      kuji: "おみくじ",
      kujis: ['大吉','中吉','小吉','末吉'],
      //style
      myStyle:{
        color: 'skyblue'
      },
      newStyle:{
        'font-weight': 'normal'
      }
    }
  },
  methods: {
    ev01(){
    this.kuji = this.kujis[Math.floor(Math.random() * this.kujis.length)]
    },
    ev02(){
      this.size += .1
    },
    ev03(){
      this.size -= .1
    },
    ev04(value){
      this.size += value
    },
    ev05(){
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>