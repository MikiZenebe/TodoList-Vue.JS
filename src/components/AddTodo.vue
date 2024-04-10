<script setup>
import { ref, computed, watch, onMounted } from "vue";

const todos = ref([]);
const inputContent = ref("");
const inputCategory = ref(null);
</script>

<template>
  <div class="flex flex-col gap-2">
    <form @submit.prevent="addTodo" class="flex flex-col gap-2">
      <div class="flex flex-col gap-1">
        <p class="text-sm font-semibold text-gray-600">
          What's on your todo list?
        </p>
        <input
          class="w-full transition-all duration-[300ms] ease-out rounded-md appearance-none border border-gray-200 py-1 px-2 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-pink-400 focus:border-transparent placeholder:text-sm"
          type="text"
          placeholder="e.g. make a food"
          v-model="inputContent"
        />
      </div>

      <div class="flex flex-col gap-1">
        <p class="text-sm font-semibold text-gray-600">Pick a category</p>

        <div class="flex items-center w-full mx-auto justify-center gap-5">
          <label
            class="flex flex-col items-center bg-white p-5 w-full rounded-md"
          >
            <input
              class="hidden"
              type="radio"
              name="category"
              value="business"
              v-model="inputCategory"
            />
            <span class="bubble business"></span>
            <p class="text-sm">Business</p>
          </label>
          <label
            class="flex flex-col items-center bg-white p-5 w-full rounded-md"
          >
            <input
              class="hidden"
              type="radio"
              name="category"
              value="personal"
              v-model="inputCategory"
            />
            <span class="bubble personal"></span>
            <p class="text-sm">Personal</p>
          </label>
        </div>

        <button
          class="mt-5 bg-[#f5379ff1] p-2 rounded-lg text-white font-semibold hover:bg-white hover:text-[#f5379ff1] hover:outline outline-1 transition-all 0.5s ease-in-out hover:border-[#f5379ff1]"
          type="submit"
          value="Add todo"
        >
          Add Todo
        </button>
      </div>
    </form>
  </div>
</template>
