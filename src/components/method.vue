<template>
  <div class="">
    <button class="btn" @click="ev01()">Button</button>
    <h1>{{ msg }}</h1>
    <h2>{{ kuji }}</h2>
 </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome',
      kuji: "kuji",
      kujis: ['大吉','中吉','小吉','末吉']
    }
  },
  methods: {
    ev01(){
      alert("hoge")
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