<template>
  <section class="hero-section">
    <component-hero />
  </section>
  <section class="our-solutions-section">
    <component-our-solutions />
  </section>
  <!--  <section class="special-section">-->
  <!--    <component-special />-->
  <!--  </section>-->
  <section class="testimonial-section"></section>
  <section class="rating-section"></section>
</template>

<script setup>
import ComponentHero from "components/homepage/ComponentHero.vue";
import ComponentOurSolutions from "components/homepage/ComponentOurSolutions.vue";
import ComponentSpecial from "components/homepage/ComponentSpecial.vue";
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

.our-solutions-section {
  position: relative;
  top: 700px;
}

.special-section {
  position: relative;
  top: 110vh;
  background-image: url("src/assets/homepage/special/special-section-bg.svg");
  background-repeat: no-repeat;
  background-position: left;
  width: 100vw;
  height: 600px;
}
</style>
