<template>
  <ul>
    <ToDoListItem
      v-for="todo in todos"
      :key="todo.id"
      :item="todo"
      @toogle="toogleListItem"
    />
  </ul>
</template>

<script>
import ToDoListItem from "./ToDoListItem";

export default {
  name: "ToDoList",
  data: () => ({
    todos: [
      { id: 1, finished: false, name: "TODO 1" },
      { id: 2, finished: false, name: "TODO 2" },
      { id: 3, finished: false, name: "TODO 3" },
      { id: 4, finished: true, name: "TODO 4" },
    ],
  }),
  components: {
    ToDoListItem,
  },
  methods: {
    toogleListItem(el) {
      el.finished = !el.finished;
    },
  },
};
</script>

<style></style>
