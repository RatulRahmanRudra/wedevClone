<template>
  <div class="q-pa-md">
    <q-btn icon="o_menu" flat @click="triggerDrawer"/>
     <q-card class="drawer" v-if="drawer">
       <q-scroll-area style="max-height: 80vh; width: 80vw; height: 52vh">
       <router-link v-for="link in links" :key="link.id" :to="link.to"  class="text-accent" :class="link.class">
         <q-separator v-if="link.id !== 1" inset/>
         <q-card-section class="q-ma-xs">{{ link.name }}</q-card-section>

       </router-link>
       </q-scroll-area>
     </q-card>

  </div>
</template>


<script setup>

import {ref} from "vue";

const props = defineProps(["links"])

const drawer = ref(false)
const triggerDrawer = () => {
  drawer.value = !drawer.value
}

</script>


<style scoped >
.drawer{
  max-height: 80vh;
  width: 80vw;
  position: absolute;
  left: 10vw;
  z-index: 1;
  background-color: white;
}
</style>
