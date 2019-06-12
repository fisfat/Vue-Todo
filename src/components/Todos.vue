<template>
  <div>
    <h1>Todos</h1>
    <h4 v-for="todo in getTodos" :key="todo.id">{{todo.title}}</h4>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";
export default {
  name: "Todos",
  computed: {
    ...mapGetters(["getTodos"])
  },
  methods: {
    ...mapActions(["fetchTodos"])
  },
  created() {
    this.fetchTodos();
  }
};
</script>

<style>
</style>
