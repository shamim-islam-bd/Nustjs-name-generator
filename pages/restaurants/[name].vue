<script setup lang="ts">
import restaurants from "@/data.json";

const route = useRoute();
const name = route.params.name;

const restaurant = restaurants.filter((r) => r.name === name);
console.log(restaurant);
</script>

<template>
  <div class="container">
    <div class="card mt-5">
      <div class="row g-0" v-if="restaurant[0]">
        <div class="col-md-4">
          <img
            :src="restaurant[0].imageUrl"
            class="img-fluid rounded-start"
            alt="..."
          />
        </div>
        <div class="col-md-8">
          <div class="card-body">
            <h5 class="card-title">{{ restaurant[0].name }}</h5>
            <p class="card-text">
              {{ restaurant[0].content }}
            </p>
            <p class="card-text">
              <small class="text-muted"
                >Store: {{ restaurant[0].numberOfStores }}</small
              >
              <br />
              <small class="text-muted">Last updated 3 mins ago</small>
            </p>
          </div>
        </div>
      </div>
      <div class="row" v-else>
        <h1>restaurant Not Found!</h1>
        <button class="btn btn-primary" @click="$router.push('/restaurants')">
          Go Back
        </button>
      </div>
    </div>
  </div>
</template>
