<template>
  <div>
    <div v-for="p in products">
      <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
    </div>
  </div>
</template>

<script>
definePageMeta({
  layout: "products",
});
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>
