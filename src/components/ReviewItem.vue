<template>
  <Card>
    <button class="close">
      <i class="fas fa-times"></i>
    </button>
    <button class="edit">
      <i class="fas fa-edit"></i>
    </button>
    <div class="num-display">
      <!-- {{ item }} -->
      5
    </div>
    <div class="text-display">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia, ab.
    </div>
  </Card>
</template>
<script setup>
import Card from "./shared/Card.vue";
</script>
