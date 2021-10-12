<template>
  <div id="app">
    <h1>Hello !! - {{ name }}</h1>
    <h1 v-bind:class="isPromoted && 'promoted'">Promoted Class View</h1>
    <p class="underline" v-bind:class="status">Greetings !! - {{ greet }}</p>
    <div v-html="email"></div>
    <div v-html="hack"></div>
    <div v-bind:id="headId">Something is ID by my Data head ID</div>
    <button v-bind:disabled="isDisable">disabled Button</button>
    <h4 v-bind:class="isPromoted ? 'promoted' : 'underline'">
      Testing Ternary Operator
    </h4>
    <p v-bind:class="['underline', 'promoted']">Array Classes By Bind</p>
    <p
      v-bind:class="{
        promoted: isPromoted,
        underline: !soldOut,
        'bg-fine': soldOut,
      }"
    >
      Object Conditional Methods CSS class
    </p>
    <p v-bind:style="headerStyleObj">Text Inline Style</p>
    <p v-bind:style="[headerStyleObj, otherSytles]">Both in Array</p>
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
      headId: "something",
      isDisable: true,
      status: "success",
      isPromoted: true,
      soldOut: true,
      heighlight: "orange",
      uppercase: true,
      headerStyleObj: {
        background: "red",
        border: "1px solid black",
        padding: "10px",
      },
      otherSytles: {
        color: "#000",
        borderRadius: "5px",
        textTransform: "capitalize",
      },
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
