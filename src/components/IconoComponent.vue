<script setup>
    import {ref} from 'vue';

    const iconos = ref([ 
        { vinculo: 'icono-sonido.svg', alternativo: 'imagen icono', titulo: 'Gran Sonido',
            parrafo: 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Duisconvallis porttitor sodales. Duis accumsan lorem neque.'},
        { vinculo: 'icono-garantia.svg', alternativo: 'imagen icono', titulo: 'Garantía de por vida',
            parrafo: 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Duisconvallis porttitor sodales. Duis accumsan lorem neque.' },
        { vinculo: 'icono-bateria.svg', alternativo: 'imagen icono', titulo: '+20 Horas de Bateria',
            parrafo: 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Duisconvallis porttitor sodales. Duis accumsan lorem neque.' }
    ])

</script>


<template>

    <section class="contenedor">

        <div class="iconos">
            <div v-for="icono in iconos" :key="icono.vinculo"  class="icono">
                <img :src="`/assets/img/${icono.vinculo}`" :alt="icono.alternativo">
                <h3>{{icono.titulo}}</h3>
                <p>{{ icono.parrafo }}</p>
            </div>

        </div>
    </section>

</template>

<style scoped></style>