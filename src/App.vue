<template>
  <div class="menu">
    <a v-for="x in menu" :key="x">{{ x }}</a>
  </div>
  <div>
    <h4 v-for="(y,i) in products" :key="y">{{ products[i] }}<p>50만원</p></h4>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      money:[50,60,70],
      menu:['Home', 'Shop', "About"],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
    }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu{
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding:10px;
}
</style>
