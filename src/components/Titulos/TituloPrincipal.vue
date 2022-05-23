<template>
    <h1 id="tituloPrincipal">{{tituloOut}}</h1>
</template>

<script>
export default {
    name: 'TituloPrincipal',
    props: {
        tituloOut: String
    }
}
</script>

<style scoped>
    #tituloPrincipal {
        font-family: "fuenteTitulos";
        animation: title-color-change 5s infinite;
    }

    @keyframes title-color-change {
        0% {color: rgb(255, 255, 255);}
        25% {color: rgb(225, 255, 252);}
        50% {color: rgb(150, 255, 243);}
        75% {color: rgb(225, 255, 252);}
        100% {color: rgb(255,255,255);}
    }

</style>