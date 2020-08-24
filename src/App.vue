<template>
  <div id="app">
   <!-- <img src="./assets/logo.png"> -->
    <Method/>
    <Time/>
    <Object/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld'
import Method from './components/method'
import Time from './components/Time'
import Object from './components/Object'

export default {
  name: 'App',
  components: {
    Method,
    Time,
]   Object 
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>