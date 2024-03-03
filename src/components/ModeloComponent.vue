<script setup>
import { ref } from 'vue';
// Define el array de modelos
const modelos = ref([
  { id: 'x', nombre: 'TechPRO X', precio: '$299' },
  { id: 'y', nombre: 'TechPRO Y', precio: '$399' },
  { id: 'z', nombre: 'TechPRO Z', precio: '$499' },

]);
</script>

<template>
    <main class="contenedor modelos">
        <h2 class="text-center degradado-verde header-modelos">Elige tus TechPRO</h2>
        <div class="listado-modelos">
        <div v-for="modelo in modelos" :key="modelo.id" :class="`modelo modelo-${modelo.id}`">
            <h3>{{ modelo.nombre }}</h3>
            <p class="precio">{{ modelo.precio }}</p>
        </div>
    </div>
    </main>


</template>

<style scoped></style>