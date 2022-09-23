<script setup>
// useMeta({
//   title: restaurant.values ? name : "404- Resaurant Not Found",
//   meta: [
//     {
//       name: "viewport",
//       content: "width=device-width, initial-scale=1.0",
//     },
//   ],
// });
</script>

<template>
  <div>
    <div class="container text-center mt-5">
      <NuxtLayout name="error">
        <template #header>
          <h1>Page Not Found</h1>
        </template>

        <template #btnRedirect>
          <NuxtLink to="/restaurants">Go back</NuxtLink>
        </template>
      </NuxtLayout>
    </div>
  </div>
</template>

<style scoped></style>
