<template>
    <main class="wrapper">
        <h1>Products</h1>
        <div class="card-container">
          <ProductCard v-for="(product, index) in inventory.slice(0,6)" :key="product.id" :index="index" class="card" :product="product" :addToCart="addToCart">
            <button @click="addToCart(product.name, i)" class="btn btn-light">
              Add to cart
            </button>
          </ProductCard>
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
