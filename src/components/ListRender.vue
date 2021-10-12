<template>
  <div id="app">
    <p v-for="(row, index) in names" :key="row">{{ index }} {{ row }}</p>

    <p v-for="name in fullname" :key="name.first">
      {{ name.first }} {{ name.last }}
    </p>

    <hr />
    <h1>Actors</h1>
    <h3 v-for="actor in actors" :key="actor.name">
      <u> {{ actor.name }} </u>
      <p v-for="movie in actor.movies" :key="movie">{{ movie }}</p>
    </h3>

    <p v-for="(info, key, index) in myinfo" :key="info">
      {{ key }} - {{ index }} - {{ info }}
    </p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Ridoy", "Guy", "Mohammad", "Tisha"],
      fullname: [
        { first: "Ridoy", last: "Islam" },
        { first: "Farzana", last: "Akter" },
        { first: "Billu", last: "Islam" },
        { first: "Guy", last: "DeGiaCinto" },
        { first: "Andy", last: "Tamson" },
      ],
      actors: [
        {
          name: "Sakib Khan",
          movies: ["batman", "superman"],
        },
        {
          name: "Ananta Jalil",
          movies: ["Basic", "default"],
        },
        {
          name: "Misa Sawdagar",
          movies: ["Red Light", "Green Light"],
        },
      ],
      myinfo: {
        name: "RIdoy",
        email: "hridoy4t@gmail.com",
        phone: "880167578981",
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
