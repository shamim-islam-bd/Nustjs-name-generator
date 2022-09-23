<script setup lang="ts"></script>

<template>
  <div>
    <Html :lang="dynamic > 50 ? 'en-GB' : 'en-US'">
      <Head>
        <Title> Restaurent </Title>
        <Meta name="description" content="This is a description of the page">
        </Meta>
        <Link rel="" />
      </Head>
    </Html>
    <div class="container text-center mt-5">
      <h1>WelCome to Restaurent</h1>
      <a href="/restaurants">Go to Restaurent</a>
    </div>
  </div>
</template>

<style scoped></style>
