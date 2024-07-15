<script lang="ts">
import type { PropType } from 'vue';
import type { Product } from './Product';

export default {
    props: {
        product: {
            type: Object as PropType<Product>,
                required: true
        }
    },
    emits: ['addProduct'],
    methods: {
        onAddButtonClick() {
            this.$emit('addProduct');
        }
    }
}
</script>

<template>
    <p>Name: {{ product.name }}</p>
    <p>Price: {{ product.price }}</p>
    <button v-on:click="onAddButtonClick"> <!-- this is another example of a short hand where im using @ instead of v-on -->
        Agregar al carrito
    </button>
    <hr />
</template>
