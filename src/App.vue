<template>
  <div id="app">
  <ul>
        <li v-for="item in itemlis">{{ item.title }}</li>
    </ul>
  </div>
</template>

<script>
import Vue from'vue'
import  VueResource  from 'vue-resource'

Vue.use(VueResource)
export default {
  name: 'HelloWorld',

   created:function(){
     this.$http.get('api/seller').then((res)=>{
         var arrJson=JSON.parse(res.bodyText)
         this.itemlis=arrJson.data.list  //注意使用箭头函数才可用this不然需要在函数外先定义变量把this赋值给变量
         console.log(this.itemlis)
     },function(err){
         console.log(err)
     })
   },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      itemlis:[],
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
