<script setup>
import { defineProps } from "vue";

const props = defineProps({
  todos: {
    type: String,
    required: true,
  },

  removeTodo: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="mt-5">
    <div>
      <h2>Todo Lists</h2>

      <div class="flex flex-col gap-2">
        <div
          v-for="todo in todos"
          :key="todo"
          :class="`flex items-center justify-around p-2 rounded-md bg-white ${
            todo.done && 'bg-gray-300 text-gray-400'
          }`"
        >
          <div class="flex items-center gap-3">
            <label>
              <input hidden type="checkbox" v-model="todo.done" />
              <span :class="`bubble cursor-pointer ${todo.category}`"></span>
            </label>

            <div>
              <input
                class="border-none bg-transparent outline-none"
                type="text"
                v-model="todo.content"
              />
            </div>
          </div>

          <div>
            <button
              @click="removeTodo(todo)"
              class="text-[10px] bg-red-500 p-1 text-white rounded-md font-semibold"
            >
              Delete
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
