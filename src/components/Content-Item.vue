<template>
    <div id="Content-Root">
        <InicioContenidoItem tituloOut="Sergio Moyano"/>
        <SobreMiItem/>
        <HabilidadesItem/>
        <ProyectosItem/>
        <ContactoItem/>
    </div>
    
</template>

<script>
// Importamos componentes de CONTENIDO
import InicioContenidoItem from '/src/components/Contenido/InicioContenido-Item.vue'
import SobreMiItem from '/src/components/Contenido/SobreMi-Item.vue'
import HabilidadesItem from '/src/components/Contenido/Habilidades-Item.vue'
import ProyectosItem from '/src/components/Contenido/Proyectos-Item.vue'
import ContactoItem from '/src/components/Contenido/Contacto-Item.vue';

// Importamos componentes de botones

require('../assets/css/Content-Item.css');

export default {
    name: 'Content-Item',
    components: {
        InicioContenidoItem,
        SobreMiItem,
        HabilidadesItem,
        ProyectosItem,
        ContactoItem
    }
}
</script> 