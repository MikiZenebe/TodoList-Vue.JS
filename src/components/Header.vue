<script setup>
import { ref, watch, onMounted } from "vue";

const name = ref("");

watch(name, (newVal) => {
  localStorage.setItem("name", newVal);
});
onMounted(() => {
  name.value = localStorage.getItem("name") || "";
});
</script>

<template>
  <div>
    <h2 class="text-xl font-semibold">
      What's up,
      <input
        class="border-none bg-slate-100 outline-none text-[#bd1672bd]"
        type="text"
        placeholder="Name here"
        v-model="name"
      />
    </h2>
  </div>
</template>
