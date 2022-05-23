<template>
    <h2 id="tituloContenido">{{tituloOut}}</h2>
</template>

<script>
export default {
    name: 'TituloContenido',
    props: {
        tituloOut: String
    }
}
</script>

<style scoped>
    #tituloContenido {
        font-family: "fuenteTitulos";
        font-weight: 100;
    }
</style>