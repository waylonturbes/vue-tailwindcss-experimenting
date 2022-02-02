<script>
import { ref } from "vue";

export default {
  setup() {
    const username = ref("");
    const password = ref("");
    return {
      username,
      password,
    };
  },
};
</script>

<template>
  <form>
    <h1>{{ username + password }}</h1>
    <div>
      <label for="username">Username</label>
      <input id="username" type="text" v-model="username" />
    </div>
    <div>
      <label for="password">Password</label>
      <input id="password" type="text" v-model="password" />
    </div>
    <div>
      <button @click="submitForm" :disabled="username.length == 0">
        Submit
      </button>
    </div>
  </form>
</template>

<style scoped></style>
