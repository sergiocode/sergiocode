<template>
    <div id="Tarjeta-Root" tituloOut="{{ tituloOut }}" class="tarjeta">
        <h3>{{tituloOut}}</h3>
    </div>
</template>

<script>
require('../../assets/css/Habilidades-Item.css');
require('../../assets/css/Tarjeta-Habilidad.css');

export default {
    name: 'Tarjeta-Habilidad',
    props: {
        tituloOut: String
    }
}
</script>