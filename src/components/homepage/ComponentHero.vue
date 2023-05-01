<template>
  <div class="row justify-between container">
    <div class="col-xs-12 col-sm-12 col-md-6 hero-left">
      <div class="text-h3 catchphrase">
        We Create Innovative Tools to Empower Businesses Around the World
      </div>

      <p class="text-accent text-subtitle1 sub-text">
        weDevs is the maker of
        <vue-typewriter-effect :strings="typeWriteTexts" />
      </p>

      <q-card style="width: 70%" class="q-mt-xl text-center">
        <q-card-section>
          Empowering <b>520,000+</b> Businesses with Innovation
        </q-card-section>
        <q-card-section>
          <q-icon name="compass" size="30px" />
          <q-icon name="compass" size="30px" />
          <q-icon name="compass" size="30px" />
          <q-icon name="compass" size="30px" />
          <q-icon name="compass" size="30px" />
          <q-icon name="compass" size="30px" />
          <q-icon name="compass" size="30px" />
        </q-card-section>
      </q-card>
    </div>

    <div class="col-xs-12 col-sm-12 col-md-6 hero-right">
      <q-img
        sizes="sm-20px"
        class="hero-img-animation"
        :src="require('assets/homepage/products/dokan.webp')"
        height="100px"
        width="100px"
        style="z-index: 1; left: 40px; top: 367px"
      />
      <q-img
        class="hero-img-animation"
        :src="require('assets/homepage/products/user-frontend.webp')"
        height="95px"
        width="95px"
        style="z-index: 1; position: relative; top: 580px; left: 55px"
      />
      <q-img
        class="hero-img-animation"
        :src="require('assets/homepage/products/wemail.webp')"
        height="50px"
        width="50px"
        style="z-index: 1; position: relative; left: 360px; top: 200px"
      />
      <q-img :src="require('src/assets/homepage/hero-feature-img.webp')" />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import VueTypewriterEffect from "vue-typewriter-effect";

const typeWriteTexts = ref([
  "Dokan Multivendor",
  "WP Project Manager",
  "WP User Frontend",
  "WP ERP",
]);
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Lato&display=swap");

.container {
  /*background-color: blue;*/
  box-sizing: border-box;
  position: relative;
  top: 120px;
  margin: auto;
  height: 600px;
  width: 100vw;
}

.hero-left,
.hero-right {
  padding: 0 50px;
}

.hero-left {
}

.catchphrase {
  font-family: "Lato", sans-serif;
  width: 70%;
  font-weight: 800;
  line-height: 1.5;
}

.sub-text {
  font-family: "Lato", sans-serif;
  font-weight: 600;
  line-height: 1.5;
  text-align: center;
  max-width: 70%;
}

@keyframes mover {
  0%,
  100% {
    transform: translateY(1px);
  }
  75% {
    transform: translateY(-1px);
  }
  50% {
    transform: translateY(-2px);
  }
}

.hero-img-animation {
  animation: mover 1s ease alternate;
  animation-duration: 1s;
  animation-timing-function: ease-out;
  animation-delay: 1s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-fill-mode: none;
  animation-play-state: running;
  animation-name: mover;
}
</style>
