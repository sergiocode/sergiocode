<template>
    <div id="SobreMi-Root" class="contenido-item">
        
        <div class="container-sobre-mi">
            <TituloPrincipal tituloOut="SERGIO MOYANO"/>
            <div class="contenedor-texto-video">
                <p class="texto-sobreMi">¡Hola! Mi nombre es Sergio Moyano y tengo 21 años. Soy un desarrollador web junior que ama diseñar interfaces intuitivas y dinámicas.<br/>
                Crecí rodeado de ordenadores y tecnología, así que decidí hacer de un hobbie una profesión.
                </p>
                <!-- Meter VIDEO INTERACTIVO-->
                <video id="video" ref="video" autobuffer controls class="video">
                    <source id="mp4" src="../../assets/video/video.mp4" type="video/mp4">
                </video>
                <div class="botonera-video">
                    <button class="control-button" @click="playVideo()"><img src="../../assets/img/play.png"></button>
                    <!-- 0:00 -->
                    <button class="section-button" @click="quienSoy()">¿Quien soy?</button>
                    <!-- 0:22 -->
                    <button class="section-button" @click="skills()">Skills</button>
                    <!-- 0:26 -->
                    <button class="section-button" @click="lenguajes()">Lenguajes</button>
                    <!-- 0:50 -->
                    <button class="section-button" @click="objetivos()">Objetivos</button>
                    <!-- 1:00 -->
                    <button class="section-button" @click="personal()">Personal</button>
                </div>
            </div>
            <ol>
                <ul v-for="dato in datosSkills" :key="dato.correo">{{dato.creativo}}</ul>
                <ul v-for="dato in datosSkills" :key="dato.correo">{{dato.entusiasta}}</ul>
                <ul v-for="dato in datosSkills" :key="dato.correo">{{dato.autodidacta}}</ul>
                <ul v-for="dato in datosSkills" :key="dato.correo">{{dato.constante}}</ul>
                <ul v-for="dato in datosSkills" :key="dato.correo">{{dato.emprendedor}}</ul>
                <ul v-for="dato in datosSkills" :key="dato.correo">{{dato.persistente}}</ul>
            </ol>
            <BotonPrincipal :href="`${publicPath}documents/Sergio Moyano CV.pdf`" download="Sergio Moyano CV.pdf" nombre="Descargar CV"></BotonPrincipal>
        </div>
    </div>
</template>

<script>
// Importo titulo de contenido
import TituloPrincipal from '/src/components/Titulos/TituloPrincipal';
import TituloContenido from '/src/components/Titulos/TituloContenido';
import BotonPrincipal from '/src/components/Botones/Boton-Principal';
import datos from '../../json/datosContacto.json';
require('../../assets/css/SobreMi-Item.css');

export default {
    name: 'SobreMi-Item',
    components: {
        TituloPrincipal,
        TituloContenido,
        BotonPrincipal
    },
    data () {
        return {
            datosSkills: datos,
            publicPath: process.env.BASE_URL
        }
    },
    methods: {
        playVideo() {
            let videoElement = document.getElementById("video");
            if (videoElement.paused) {
                videoElement.play()
            } else {
                videoElement.pause();
            }
        },
        quienSoy() {
            let videoElement = document.getElementById("video");
            videoElement.currentTime = 0;
            videoElement.play();
        },
        skills() {
            let videoElement = document.getElementById("video");
            videoElement.currentTime = 21;
            videoElement.play();
        },
        lenguajes() {
            let videoElement = document.getElementById("video");
            videoElement.currentTime = 26;
            videoElement.play();
        },
        objetivos() {
            let videoElement = document.getElementById("video");
            videoElement.currentTime = 50;
            videoElement.play();
        },
        personal() {
            let videoElement = document.getElementById("video");
            videoElement.currentTime = 60;
            videoElement.play();
        }
    },
}
</script>