<script setup lang="ts">
import { Ref, ref, watch, computed, onMounted } from "vue";
import Users from "@/components/Users.vue";

import { User } from "./types";

import api from "@/api";

const users: Ref<User[]> = ref([]);

const fetchUser = async () => {
  try {
    const response = await api.get<User[]>("/users");
    users.value = response.data;
  } catch (error) {
    console.log(error);
  }
};

onMounted(async () => {
  await fetchUser();
});
</script>

<template>
  <div>
    <Users :users="users" />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
