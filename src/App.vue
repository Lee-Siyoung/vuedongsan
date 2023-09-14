<template>
  <div class="menu">
    <a v-for="x in menu" :key="x">{{ x }}</a>
  </div>
  <div>
    <h4>{{ products[0] }}</h4>
    <p>50만원</p>
    <button @click="increase">허위매물신고</button>
    <span>신고수 : {{ Declar }}</span>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>50만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>50만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      Declar: 0,
      money: [50, 60, 70],
      menu: ["Home", "Shop", "About"],
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },
  methods: {
    increase() {
      this.Declar += 1;
    },
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
