<template>
    <div id="Habilidades-Root" class="contenido-item">
        <TituloContenido tituloOut="HABILIDADES"/>
        <div class="tarjetas-habilidades">
            <div class="habilidades-contenido">
                <p class="texto-habilidades">Domino lenguajes tanto frontend como backend, además de frameworks. También hago uso de bases de datos
                relacionales (SQL) y no relacionales como Mongo DB.
                </p>
                <div class="tarjetas">
                    <div id="tarjeta-frontend" class="tarjeta-vertical">
                        <h3>FRONTEND</h3>
                        <ol class="listado-habilidades">
                            <ul><img src="../../assets/img/html.png" alt="No es posible visualizar la imagen"/>HTML</ul>
                            <ul><img src="../../assets/img/css.png" alt="No es posible visualizar la imagen"/>CSS & SASS</ul>
                            <ul><img src="../../assets/img/js.png" alt="No es posible visualizar la imagen"/>JavaScript</ul>
                            <ul><img src="../../assets/img/vue.png" alt="No es posible visualizar la imagen"/>Vue</ul>
                            <ul><img src="../../assets/img/react.png" alt="No es posible visualizar la imagen"/>React JS</ul>
                        </ol>
                    </div>
                    <div id="tarjeta-backend" class="tarjeta-vertical">
                        <h3>BACKEND</h3>
                        <ol class="listado-habilidades">
                            <ul><img src="../../assets/img/java.png" alt="No es posible visualizar la imagen"/>Java</ul>
                            <ul><img src="../../assets/img/php.png" alt="No es posible visualizar la imagen"/>PHP</ul>
                            <ul><img src="../../assets/img/laravel.png" alt="No es posible visualizar la imagen"/>Laravel</ul>
                            <ul><img src="../../assets/img/sql.png" alt="No es posible visualizar la imagen"/>SQL</ul>
                            <ul><img src="../../assets/img/mongo.png" alt="No es posible visualizar la imagen"/>Mongo DB</ul>
                        </ol>
                    </div>
                </div>
                <p class="texto-habilidades">Tengo conocimientos avanzados en el ámbito de la multimedia, ya que hago mis propios logos, edito imagen y vídeo e incluso diseño
                sonidos para implementar en mis proyectos. Para ello hago uso de la suite de Adobe y programas como Logic Pro y Cubase.
                </p>
                <div class="tarjetas">
                    <div class="tarjeta-horizontal">
                        <div class="container-idioma">
                            <img src="../../assets/img/castellano.png" alt="No es posible visualizar la imagen"/>
                            <div class="nivel">Castellano NATIVO</div>
                        </div>
                        <div class="container-idioma">
                            <img src="../../assets/img/catalan.png" alt="No es posible visualizar la imagen"/>
                            <div class="nivel">Catalán NATIVO</div>
                        </div>
                        <div class="container-idioma">
                            <img src="../../assets/img/ingles.png" alt="No es posible visualizar la imagen"/>
                            <div class="nivel">Inglés NIVEL B2</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
// Importo titulo de contenido
import TituloContenido from '/src/components/Titulos/TituloContenido';
import TarjetaHabilidad from '/src/components/Tarjetas/Tarjeta-Habilidad';
require('../../assets/css/Habilidades-Item.css');

export default {
    name: 'Habilidades-Item',
    components: {
        TituloContenido,
        TarjetaHabilidad
    },
    props: {
        tituloOut: String
    }
}
</script>