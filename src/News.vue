<template>
  <div id="app">
   <h3>Welcome Vue-webpack</h3>
   <strong>{{msg}}</strong>
  </div>
</template>

<script>
export default{
	data(){
		return {
			msg:'welcome'
		}
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
