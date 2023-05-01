<template>
  <q-layout view="hHr lpr fFf">
    <component-header />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import ComponentHeader from "components/ComponentHeader.vue";
</script>
