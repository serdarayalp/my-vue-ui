<template>
  <li :class="{ finishedTask: item.finished }">
    <input type="checkbox" v-bind:checked="item.finished" />
    <button @click="toogleItem">toogle</button>
    {{ item.name }}
  </li>
</template>

<script>
export default {
  name: "ToDoListItem",
  props: ["item"],
  methods: {
    toogleItem() {
      this.$emit("toogle", this.item);
    },
  },
};
</script>

<style></style>
