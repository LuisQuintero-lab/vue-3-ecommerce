<script setup lang="ts">
    import { onMounted, ref } from 'vue'

    const count = ref(0);

    function increase() {
        count.value += 1;
    }

    function decrease() {
        if(count.value > 0){
            count.value -= 1;
        }
        
    }

    onMounted( () => {
        console.log('El valor inicial del contador es ' + count.value);
    } );
</script>

<template>
    <p>Composition API version of vue</p>
    <h1>Contador: {{ count }}</h1>

    <button @click="increase">
        Incrementar contador
    </button>
    <button @click="decrease">
        Disminuir contador
    </button>

</template>