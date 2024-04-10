<script setup></script>

<template>
  <div class="flex flex-col gap-2">
    <div class="flex flex-col gap-1">
      <p class="text-sm font-semibold text-gray-600">
        What's on your todo list?
      </p>
      <input
        class="w-full transition-all duration-[300ms] ease-out rounded-md appearance-none border border-gray-200 py-1 px-2 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-pink-400 focus:border-transparent placeholder:text-sm"
        type="text"
        placeholder="e.g. make a food"
      />
    </div>

    <div class="flex flex-col gap-1">
      <p class="text-sm font-semibold text-gray-600">Pick a category</p>

      <div class="flex items-center w-full mx-auto justify-center gap-5">
        <label
          class="flex flex-col items-center bg-white p-5 w-full rounded-md"
        >
          <input class="hidden" type="radio" name="" id="" />
          <span class="bubble business"></span>
          <p class="text-sm">Business</p>
        </label>
        <label
          class="flex flex-col items-center bg-white p-5 w-full rounded-md"
        >
          <input class="hidden" type="radio" name="" id="" />
          <span class="bubble personal"></span>
          <p class="text-sm">Personal</p>
        </label>
      </div>
    </div>
  </div>
</template>
