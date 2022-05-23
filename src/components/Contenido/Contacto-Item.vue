<template>
    <div id="Contacto-Root" class="contacto-item">
        <TituloContenido tituloOut="CONTACTO"/>
        <TarjetaContacto/>
    </div>
</template>

<script>
// Importo titulo de contenido
import TituloContenido from '/src/components/Titulos/TituloContenido';
import TarjetaContacto from '/src/components/Tarjetas/Tarjeta-Contacto';
require('../../assets/css/Contacto-Item.css');

export default {
    name: 'Contacto-Item',
    components: {
        TituloContenido,
        TarjetaContacto
    }
}
</script>