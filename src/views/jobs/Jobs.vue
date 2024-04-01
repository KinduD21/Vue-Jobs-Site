<template>
  <h1 class="mb-5 text-center text-4xl font-bold text-gray-600">Jobs</h1>
  <div v-for="job in jobs" v-bind:key="job.id">
    <router-link v-bind:to="{ name: 'JobDetails', params: { id: job.id } }">
      <h2
        class="mx-auto my-3 max-w-96 cursor-pointer rounded-xl bg-slate-300 p-5 text-center text-2xl text-gray-600 hover:bg-slate-200"
      >
        {{ job.title }}
      </h2>
    </router-link>
  </div>
</template>

<script setup>
import { ref } from "vue";

const jobs = ref([
  { title: "UX Designer", id: 1, details: "lorem" },
  { title: "Web Developer", id: 2, details: "lorem" },
  { title: "Vue Developer", id: 3, details: "lorem" },
]);
</script>
