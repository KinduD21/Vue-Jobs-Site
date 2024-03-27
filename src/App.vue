<template>
  <div>
    <router-link v-bind:to="{ name: 'Home' }">Home</router-link> |
    <router-link v-bind:to="{ name: 'About' }">About</router-link>
  </div>
  <router-view />
</template>

<script setup></script>
