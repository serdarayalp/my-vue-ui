<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

  Hallo, {{ full_name }}

  <br />

  <navigation-link url="http://www.google.de">Zur Info</navigation-link>

  <br />
  <a href="?seite=123" @click.right.prevent="test">Gehe zur Seite 23</a>

  <ToDoList />

  <button v-on:click="test">Test</button>
  <!-- <button @click="test">Test-2</button> -->
</template>

<script>
import ToDoList from "./components/ToDoList";
import NavigationLink from "./components/NavigationLink";

export default {
  name: "App",
  data: () => ({
    vorname: "Serdar",
    nachname: "Ayalp",
    alter: 40,
    gender: "männlich",
  }),
  computed: {
    full_name() {
      return this.vorname + " " + this.nachname;
    },
  },
  methods: {
    test() {
      alert("Das ist ein Test...");
    },
  },
  components: {
    ToDoList,
    NavigationLink,
  },
};
</script>

<style>
@import "./assets/main.css";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.finishedTask {
  text-decoration: line-through;
}
</style>
