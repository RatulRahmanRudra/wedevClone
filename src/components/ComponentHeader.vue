<template>
  <div class="bg-transparent text-black header">
    <div
      class="row q-ma-md justify-between text-capitalize"
      style="height: 100%; width: 100%"
    >
      <div class="row col-8 justify-around">
        <router-link to="/">
          <q-img
            height="50px"
            class="float-left"
            width="100px"
            :src="require('src/assets/logo.png')"
          />
        </router-link>
        <div class="q-my-auto">
          <router-link
            v-for="link in links"
            :key="link.id"
            :to="link.to"
            class="q-mx-sm text-accent"
            :class="link.class"
          >
            <span
              class="link text-uppercase"
              v-if="link.show && $q.screen.gt.sm"
              >{{ link.name }}</span
            >
          </router-link>
        </div>
      </div>
      <div class="q-my-auto text-accent text-capitalize">
        <q-btn v-if="$q.screen.gt.sm" icon="o_shopping_cart" flat round />
        <q-btn
          v-if="$q.screen.gt.sm"
          rounded
          label="My Account"
          size="10px"
          color="primary"
          class="shadow-11 shadow-blue"
        />
      </div>
      <div>
        <component-nav-drawer v-if="$q.screen.lt.md" :links="links" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { useQuasar } from "quasar";
import ComponentNavDrawer from "components/ComponentNavDrawer.vue";

const $q = useQuasar();

const links = ref([
  {
    id: 1,
    to: "/products",
    name: "products",
    asset: "",
    class: "",
    show: true,
  },
  { id: 2, to: "/blog", name: "blog", asset: "", class: "", show: true },
  { id: 3, to: "/about", name: "about", asset: "", class: "", show: true },
  { id: 4, to: "/docs", name: "docs", asset: "", class: "", show: true },
  {
    id: 5,
    to: "/contact",
    name: "contact us",
    asset: "",
    class: "",
    show: true,
  },
  { id: 6, to: "/cart", name: "cart", asset: "", class: "", show: false },
  {
    id: 7,
    to: "/account",
    name: "my account",
    asset: "",
    class: "",
    show: false,
  },
]);
</script>

<style scoped>
.link:hover {
  color: #1976d2;
}

.header {
  background-color: transparent;
  box-shadow: none;
  position: absolute;
  top: 0;
  width: 100%;
}
</style>
