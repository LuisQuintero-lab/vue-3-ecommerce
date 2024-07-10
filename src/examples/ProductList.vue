<script lang="ts">
import type { Product } from './Product';
import ProductCard from './ProductCard.vue';

export default {
    components: {
        ProductCard
    },
    data() {
        return {
            products: <Array<Product>>[
                {id: 5, name: 'Chair', price: 56},
                {id: 7, name: 'Monitor', price: 450},
                {id: 12, name: 'Microphone', price: 120}
            ]
            
        }
    },
    methods: {
        onProductAdded(productId: number) {
            console.log('Agregar producto ' + productId);
        }
    }
}
</script>

<template>
    <ProductCard 
    v-for="p in products" 
    :product="p" 
    @addProduct="onProductAdded(p.id)"/>
</template>
