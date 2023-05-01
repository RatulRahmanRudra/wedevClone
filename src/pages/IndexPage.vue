<template>
  <section class="hero-section">
    <component-hero />
  </section>
  <section class="our-solutions-section"></section>
  <section class="special-section"></section>
  <section class="testimonial-section"></section>
  <section class="rating-section"></section>
</template>

<script setup>
import ComponentHero from "components/homepage/ComponentHero.vue";
</script>

<style scoped>
.hero-section {
  background-image: url("src/assets/homepage/hero-left-shadow.svg"),
    url("src/assets/homepage/hero-right-shadow.svg");
  background-position: left, right bottom;
  background-repeat: no-repeat, no-repeat;
  width: 100vw;
  height: 600px;
}
</style>
