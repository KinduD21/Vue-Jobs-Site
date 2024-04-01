<template>
  <h1 class="mb-5 text-center text-4xl font-bold text-gray-600">
    Job Details Page
  </h1>
  <p class="mb-5 text-center text-3xl text-gray-600">The job id is {{ id }}</p>
</template>

<script setup>
const { id } = defineProps(["id"]);
</script>
