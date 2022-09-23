<script setup lang="ts">
interface RowProps {
  idx?: number;
  rank?: number;
  name?: string;
  index?: number;
  isHeader?: boolean;
}
const props = defineProps<RowProps>();
</script>

<template>
  <div class="row" v-if="isHeader">
    <div class="header">Rank</div>
    <div class="header">Name</div>
  </div>
  <div
    v-else
    class="row"
    :style="
      idx % 2 === 0 ? { backgroundColor: 'rgba(128, 128, 128, 0.336)' } : null
    "
  >
    <p class="header rank">{{ rank }}</p>
    <NuxtLink :to="`/restaurants/${name}`" class="header link">
      {{ name }}
    </NuxtLink>
  </div>
</template>

<style scoped>
.row {
  border-top: 1px solid rgba(128, 128, 128, 0.336);
  display: flex;
  align-items: center;
}
.header {
  font-size: 1.25rem;
  color: rgb(10, 31, 148);
  margin: 0;
  margin-right: 2rem;
  padding: 0.5rem 1rem;
  font-weight: 700;
  width: 4rem;
}
.rank {
  color: black;
}
.link {
  text-decoration: none;
  color: rgb(228, 157, 27);
  width: auto;
  font-weight: 500;
}
</style>
