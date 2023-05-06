<template>
  <div class="grid-item" :class="props.isMiddle && 'middle'">
    <img
      src="https://picsum.photos/200"
      style="max-width: 100%; max-height: 100%"
    />
    <div class="q-pa-lg">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab, repellat?
    </div>
    <span class="q-ma-lg">learn more</span>
  </div>
</template>

<script setup>
const props = defineProps(["isMiddle"]);
</script>

<style scoped>
.grid-item {
  position: relative;
  background-color: whitesmoke;
  padding: 20px;
  text-align: center;
  transition: transform 0.3s ease;
}

.grid-item:hover {
  background-color: rgba(245, 245, 245, 0.94);
  transform: translateY(-5px);
}

.middle {
  transform: translateY(-40px);
}

.middle:hover {
  background-color: rgba(245, 245, 245, 0.94);
  transform: translateY(-45px);
}

@media (max-width: 768px) {
  .middle {
    transform: none;
  }
}
</style>
