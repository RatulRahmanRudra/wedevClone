<template>
  <router-view />
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
});
</script>

<style>
a {
  color: inherit;
  text-decoration: none; /* no underline */
}

body {
  margin: 0;
  padding: 0;
}
</style>
