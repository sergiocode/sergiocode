<template>
    <div id="Proyectos-Root" class="contenido-item">
        <TituloContenido class="titulo-proyectos" tituloOut="PROYECTOS"/>
        <div class="explicacion-proyectos">
            <p>Estos son algunos de los proyectos que he hecho a lo largo de mi carrera como desarrollador. La mayoría de ellos son proyectos y trabajos que hice mientras estudiaba:</p>
        </div>
        <div class="contenedor-proyectos">
            <a id="Tarjeta-Proyecto" class="proyecto-tarjeta" href="https://sergiocode.github.io/FraseGame/">
                <img class="imagen-tarjeta" src="../../assets/img/portadaFrase.png" alt="No es posible visualizar la imagen"/>
                <div class="footer-tarjeta">
                    <h3>Juego FRASE</h3>
                </div>
            </a>
            <a id="Tarjeta-Proyecto" class="proyecto-tarjeta" href="https://sergiocode.github.io/M06_05_FT_01/">
                <img class="imagen-tarjeta" src="../../assets/img/eventosDOM.png" alt="No es posible visualizar la imagen"/>
                <div class="footer-tarjeta">
                    <h3>Eventos DOM</h3>
                </div>
            </a>
            <a id="Tarjeta-Proyecto" class="proyecto-tarjeta" href="https://sergiocode.github.io/DomElements/">
                <img class="imagen-tarjeta" src="../../assets/img/elementosDOM.png" alt="No es posible visualizar la imagen"/>
                <div class="footer-tarjeta">
                    <h3>Elementos DOM</h3>
                </div>
            </a>
        </div>
    </div>
</template>

<script>
// Importo titulo de contenido
import TituloContenido from '/src/components/Titulos/TituloContenido';


require('../../assets/css/Proyectos-Item.css');
require('../../assets/css/Tarjeta-Proyecto.css');


export default {
    name: 'Proyectos-Item',
    components: {
        TituloContenido
    },
    data: () => ({
        proj1: {
            titulo: "Juego FRASE",
            web: "https://sergiocode.github.io/FraseGame/"
        },
        proj2: {
            titulo: "Eventos DOM",
            web: "https://sergiocode.github.io/M06_05_FT_01/"
        },
        proj3: {
            titulo: "Elementos DOM",
            web: "https://sergiocode.github.io/DomElements/"
        }
    })
}
</script>
