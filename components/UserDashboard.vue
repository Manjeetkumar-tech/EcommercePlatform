<template>
  <div>
    <h2>Welcome to Your Dashboard</h2>
    <p>You are logged in successfully!</p>
  </div>
</template>

<script setup>
import { onMounted } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();

onMounted(() => {
  if (!localStorage.getItem("token")) {
    router.push("/login");
  }
});
</script>
