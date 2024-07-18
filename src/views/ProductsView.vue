<template>
  <main class="wrapper">
    <div class="card-container">
      <ProductCard
          v-for="(product, i) in inventory"
          :key="product.id"
          :i="i"
          :product="product"
          :addToCart="addToCart"
          class="card"
          />
    </div>
  </main>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'

export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
