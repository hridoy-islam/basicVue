<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="25%" />
    <h1>Hello !! - {{ name }}</h1>
    <h2>Greetings !! - {{ greet }}</h2>
    <div v-html="email"></div>
    <div v-html="hack"></div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Md. Ridoy ",
      greet: "Salam",
      email: "<b>hridoy4t@gmail.com</b>",
      hack: `<a href="#" onClick="alert('you have been hacked!!')">Win a Prize!!!</a>`,
    };
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
</style>
