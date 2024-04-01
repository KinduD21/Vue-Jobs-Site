<template>
  <div class="mb-5 flex items-center justify-center gap-3 p-5 text-2xl">
    <router-link class="rounded-md px-3 py-2" v-bind:to="{ name: 'Home' }"
      >Home</router-link
    >
    |
    <router-link class="rounded-md px-3 py-2" v-bind:to="{ name: 'About' }"
      >About</router-link
    >
    |
    <router-link class="rounded-md px-3 py-2" v-bind:to="{ name: 'Jobs' }"
      >Jobs</router-link
    >
  </div>

  <div class="flex justify-center">
    <button
      class="mx-3 rounded bg-slate-200 p-3 font-semibold hover:opacity-90"
      v-on:click="redirect"
    >
      Redirect
    </button>
    <button
      class="mx-3 rounded bg-slate-200 p-3 font-semibold hover:opacity-90"
      v-on:click="back"
    >
      Go back
    </button>
    <button
      class="mx-3 rounded bg-slate-200 p-3 font-semibold hover:opacity-90"
      v-on:click="forward"
    >
      Go forward
    </button>
  </div>

  <router-view />
</template>

<script setup>
import { useRouter } from "vue-router";

const router = useRouter();

function redirect() {
  router.push({ name: "Home" });
}

function back() {
  router.go(-1);
}

function forward() {
  router.go(1);
}
</script>

<style>
.router-link-active.router-link-exact-active {
  color: #fff;
  background: #dc143c;
}
</style>
