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
                    <button class="section-button" @click="quienSoy()" id="boton-quienSoy">¿QUIEN SOY?</button>
                    <!-- 0:22 -->
                    <button class="section-button" @click="skills()" id="boton-skills">SKILLS</button>
                    <!-- 0:26 -->
                    <button class="section-button" @click="lenguajes()" id="boton-lenguajes">LENGUAJES</button>
                    <!-- 0:50 -->
                    <button class="section-button" @click="objetivos()" id="boton-objetivos">OBJETIVOS</button>
                    <!-- 1:00 -->
                    <button class="section-button" @click="personal()" id="boton-personal">PERSONAL</button>
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
            let quienSoy = document.getElementById("boton-quienSoy");
            let skills = document.getElementById("boton-skills");
            let lenguajes = document.getElementById("boton-lenguajes");
            let objetivos = document.getElementById("boton-objetivos");
            let personal = document.getElementById("boton-personal");

            if (videoElement.paused) {
                videoElement.play();
            } else {
                videoElement.pause();
            }

            let i = setInterval(() => {
                if (videoElement.currentTime <= 20) {
                    quienSoy.style.backgroundColor = "rgb(59,189,174)";
                } else {
                    quienSoy.style.backgroundColor = "rgb(69 76 75)";
                }

                if (videoElement.currentTime >= 20 && videoElement.currentTime <= 26) {
                    skills.style.backgroundColor = "rgb(59,189,174)";
                } else {
                    skills.style.backgroundColor = "rgb(69 76 75)";
                }

                if (videoElement.currentTime >= 26 && videoElement.currentTime <= 49) {
                    lenguajes.style.backgroundColor = "rgb(59,189,174)";
                } else {
                    lenguajes.style.backgroundColor = "rgb(69 76 75)";
                }

                if (videoElement.currentTime >= 49 && videoElement.currentTime <= 59) {
                    objetivos.style.backgroundColor = "rgb(59,189,174)";
                } else {
                    objetivos.style.backgroundColor = "rgb(69 76 75)";
                }

                if (videoElement.currentTime >= 59 && videoElement.currentTime <= 78) {
                    personal.style.backgroundColor = "rgb(59,189,174)";
                } else {
                    personal.style.backgroundColor = "rgb(69 76 75)";
                }
            }, 100);
            i;
        },
        quienSoy() {
            let videoElement = document.getElementById("video");
            let boton = document.getElementById("boton-quienSoy");
            videoElement.currentTime = 0;
            boton.style.backgroundColor = "rgb(59,189,174)";
            videoElement.play();
            let i = setInterval(() => {
                if (videoElement.currentTime >= 21) {
                    videoElement.pause();
                    boton.style.backgroundColor = "rgb(69 76 75)";
                    clearInterval(i);
                }
            }, 500);
            i;
        },
        skills() {
            let videoElement = document.getElementById("video");
            let boton = document.getElementById("boton-skills");
            videoElement.currentTime = 21;
            boton.style.backgroundColor = "rgb(59,189,174)";
            videoElement.play();
            let i = setInterval(() => {
                if (videoElement.currentTime >= 26 || videoElement.currentTime <= 21) {
                    videoElement.pause();
                    boton.style.backgroundColor = "rgb(69 76 75)";
                    clearInterval(i);
                }
            }, 500);
            i;
        },
        lenguajes() {
            let videoElement = document.getElementById("video");
            let boton = document.getElementById("boton-lenguajes");
            videoElement.currentTime = 26;
            boton.style.backgroundColor = "rgb(59,189,174)";
            videoElement.play();
            let i = setInterval(() => {
                if (videoElement.currentTime >= 49 || videoElement.currentTime <= 26) {
                    videoElement.pause();
                    boton.style.backgroundColor = "rgb(69 76 75)";
                    clearInterval(i);
                }
            }, 500);
            i;
        },
        objetivos() {
            let videoElement = document.getElementById("video");
            let boton = document.getElementById("boton-objetivos");
            videoElement.currentTime = 50;
            boton.style.backgroundColor = "rgb(59,189,174)";
            videoElement.play();
            let i = setInterval(() => {
                if (videoElement.currentTime >= 60 || videoElement.currentTime <= 50) {
                    videoElement.pause();
                    boton.style.backgroundColor = "rgb(69 76 75)";
                    clearInterval(i);
                }
            }, 500);
            i;
        },
        personal() {
            let videoElement = document.getElementById("video");
            let boton = document.getElementById("boton-personal");
             videoElement.currentTime = 60;
            boton.style.backgroundColor = "rgb(59,189,174)";
            videoElement.play();
            let i = setInterval(() => {
                if (videoElement.currentTime >= 78 || videoElement.currentTime <= 60) {
                    videoElement.pause();
                    boton.style.backgroundColor = "rgb(69 76 75)";
                    clearInterval(i);
                }
            }, 500);
            i;
        }
    },
}
</script>