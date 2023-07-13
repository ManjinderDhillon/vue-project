<template>
  <div class="card" :class="{ reverse: reverse }">
    <slot />
  </div>
</template>
<script setup>
const props = defineProps({
  reverse: {
    type: Boolean,
    default: false,
  },
});
</script>
<style scoped>
.card {
  background-color: #fff;
  color: #212121;
}
.card.reverse {
  color: #fff;
  background-color: #212121;
}
</style>
