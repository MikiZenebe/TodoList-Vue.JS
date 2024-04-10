<script setup>
import Header from "./components/Header.vue";
import AddTodo from "./components/AddTodo.vue";
import ListTodo from "./components/ListTodo.vue";
</script>

<template>
  <div
    class="flex flex-col gap-5 bg-slate-100 p-6 rounded-lg shadow-2xl h-auto"
  >
    <Header />
    <AddTodo />
  </div>
</template>
