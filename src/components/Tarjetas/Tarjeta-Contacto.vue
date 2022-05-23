<template>
    <div id="Tarjeta-Contacto" class="tarjeta-contacto">
        <img class="foto-perfil" src="../../assets/img/fotoPerfil.jpeg"/>
        <p v-for="dato in datosContacto" :key="dato.correo">{{dato.correo}}</p>
        <p class="numero-contacto" v-for="dato in datosContacto" :key="dato.num">{{dato.num}}</p>

        <div class="redes-sociales">
            <a href="https://www.linkedin.com/in/sergio-moyano-romero-445b0b225/">
                <img src="../../assets/img/linkedin.png"/>
            </a>
            <a href="https://twitter.com/thesergiomoyano">
                <img src="../../assets/img/twitter.png"/>
            </a>
            <a href="https://www.instagram.com/thesergiomoyano/">
                <img src="../../assets/img/instagram.png"/>
            </a>
        </div>
    </div>
</template>

<script>
import datos from '../../json/datosContacto.json';
require('../../assets/css/Tarjeta-Contacto.css');

export default {
    name: 'Tarjeta-Contacto',
    data() {
        return {
            datosContacto: datos
        }
    }
}
</script>