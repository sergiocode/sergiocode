<template>
    <div id="InicioContenido-Root" class="contenido-item">
        <!-- AÑADIR LOGO PERSONAL -->
        <!-- AÑADIR <p> CON SOFT SKILL QUE VA CAMBIANDO -->
        <!-- AÑADIR LOGO O BOTON INDICANDO FLEXA ABAJO CON ANIMACION ARRIBA Y ABAJO -->
        <a href="#SobreMi-Root"><img class="flexa-abajo" src="../../assets/img/flexa-abajo.png"/></a>
    </div>
</template>

<script>
// Importo el titulo principal
import TituloPrincipal from '/src/components/Titulos/TituloPrincipal';
require('../../assets/css/InicioContenido-Item.css');

export default {
    name: 'InicioContenido-Item',
    components: {
        TituloPrincipal
    }
}
</script>