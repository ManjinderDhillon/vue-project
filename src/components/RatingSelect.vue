<template>
  <ul class="rating">
    <li v-for="n in 10" :key="`rating-${n}`">
      <input
        type="radio"
        :id="`num${n}`"
        name="rating"
        :value="n"
        :checked="selected === n"
        v-model="selected"
      />
      <label :for="`num${n}`">{{ n }}</label>
    </li>
  </ul>
</template>

<script setup>
import { ref, watch, defineEmits, defineProps } from "vue";

const props = defineProps({
  rating: {
    type: Number,
  },
});
defineEmits(["setRating"]);

const selected = ref(props.rating);

watch(selected, (newValue) => {
  emit("setRating", newValue);
});

watch(
  () => props.rating,
  (newValue) => {
    selected.value = newValue;
  }
);
</script>
