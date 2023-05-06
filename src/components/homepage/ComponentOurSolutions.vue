<template>
  <div class="container text-center">
    <div class="text-h3 text-capitalize title">
      <span class="text-blue">our </span>solution
    </div>
    <div class="sub-title q-ma-lg text-accent">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi cumque
      cupiditate eligendi esse et eveniet ex illum incidunt, laudantium maiores
      nemo numquam odio optio perferendis praesentium qui, quis quo ratione
      soluta ut veritatis voluptas voluptates? At cum distinctio doloremque ea
      fugit neque praesentium voluptate. Consectetur consequuntur dolor labore
      recusandae similique?
    </div>

    <div class="grid-container">
      <ComponentSubSolutionCard />
      <ComponentSubSolutionCard :is-middle="true" />
      <ComponentSubSolutionCard />
      <ComponentSubSolutionCard />
      <ComponentSubSolutionCard :is-middle="true" />
      <ComponentSubSolutionCard />
    </div>

    <div class="view-all-products-btn-container">
      <q-btn color="primary">View All Products</q-btn>
    </div>
  </div>
</template>

<script setup>
import ComponentSubSolutionCard from "components/homepage/sub/ComponentSubSolutionCard.vue";
</script>

<style scoped>
.container {
}

.title {
  opacity: 0.9;
  font-weight: 900;
  color: #000;
  font-size: 4rem;
  letter-spacing: 0.36px;
}

.sub-title {
  max-width: 60%;
  margin: 30px auto;
}

.grid-container {
  position: relative;
  top: 100px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
  width: 70vw;
  margin: auto;
}

.view-all-products-btn-container {
  position: relative;
  top: 200px;
  margin: auto;
  padding: 30px;
}

.view-all-products-btn-container:hover {
}

@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }

  .middle {
    transform: none;
  }
}
</style>
