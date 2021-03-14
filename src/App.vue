<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

   Hallo, {{full_name}}

  <ToDoList />

  <button v-on:click="test">Test</button>
  <!-- <button @click="test">Test-2</button> -->
</template>

<script>

import ToDoList from './components/ToDoList'

export default {
  name: "App",
  data: () => ({
    vorname: "Serdar",
    nachname: "Ayalp",
    alter: 40,
    gender: "männlich"
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
    ToDoList
  }
};
</script>

<style>

 @import './assets/main.css';

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
