<script lang="ts">
export default {
    data() {
        return {
            count: 0
        }
    },
    methods: {
        increase() {
            this.count +=1;
        },
        decrease() {
            if (this.count > 0) {
                this.count -=1;
            }   
        }
    },
    mounted() {
        console.log('El valor inicial del contador es ' + this.count);
    }
}
</script>

<template>
    <p>Objetivo llegar a 20 clicks</p>
    <h1> Contador: {{ count }} </h1>
    <button @click="increase">
        Aumentar contador
    </button>
    <button @click="decrease">
        Disminuir contador
    </button>
    <p v-if="count < 10">Let's go you can do it</p>
    <p v-else>You almost got it ......</p>
</template>
