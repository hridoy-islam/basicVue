<template>
  <div id="app">
    <h2>{{ name }}</h2>
    <button v-on:mouseover="name = 'Batman'">change name</button>

    <h2>Count {{ count }}</h2>
    <button v-on:click="increment(1)">Increment</button>
    <button v-on:click="increment(5)">Increment 5</button>
    <button v-on:click="decrement(1)">Decrement</button>
    <button v-on:click="decrement(5)">Decrement 5</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Ridoy",
      count: 0,
    };
  },
  methods: {
    increment(num) {
      return (this.count += num);
    },
    decrement(num) {
      return (this.count -= num);
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  color: red;
}
.bg-fine {
  background: #2c3e50;
}
</style>
