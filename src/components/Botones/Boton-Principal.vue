<template>
    <a class="boton-principal">{{nombre}}</a>
</template>

<script>
// Importo titulo de contenido
require('../../assets/css/Boton-Principal.css');

export default {
    name: 'Boton-Principal',
    props: {
        nombre: String
    }
}
</script>