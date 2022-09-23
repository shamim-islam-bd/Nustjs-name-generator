<template>
  <div>
    <Html :lang="dynamic > 50 ? 'en-GB' : 'en-US'">
      <Head>
        <Title> TOP 50: THE RANKING </Title>
        <Meta name="description" content="This is a description of the page">
        </Meta>
        <Link rel="" />
      </Head>
    </Html>
    <div class="container mt-5">
      <RestaurantTable />
    </div>
  </div>
</template>
