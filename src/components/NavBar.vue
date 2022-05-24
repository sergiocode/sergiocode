<template>
    <nav>
        <div class="navbar-content">
            <a href="InicioContenido-Root">
                <img src="../assets/img/logoWh.svg"/>
            </a>
            <div class="navbar-links">
                <a class="navbar-link" href="#InicioContenido-Root">INICIO</a>
                <a class="navbar-link" href="#SobreMi-Root">SOBRE MI</a>
                <a class="navbar-link" href="#Habilidades-Root">HABILIDADES</a>
                <a class="navbar-link" href="#Proyectos-Root">PROYECTOS</a>
                <a class="navbar-link" href="#Contacto-Root">CONTACTO</a>
            </div>
            <div @click="mostrarMenu()" class="icono-menu">
                <img src="../assets/img/icono-menu.svg"/>
            </div>
        </div>
    </nav>
    <div class="navbar-links-mobile">
        <a class="navbar-link" @click="cerrarNavbar()" href="#InicioContenido-Root">INICIO</a>
        <a class="navbar-link" @click="cerrarNavbar()" href="#SobreMi-Root">SOBRE MI</a>
        <a class="navbar-link" @click="cerrarNavbar()" href="#Habilidades-Root">HABILIDADES</a>
        <a class="navbar-link" @click="cerrarNavbar()" href="#Proyectos-Root">PROYECTOS</a>
        <a class="navbar-link" @click="cerrarNavbar()" href="#Contacto-Root">CONTACTO</a>
    </div>
</template>

<script>
require('../assets/css/NavBar.css');

export default {
    name: 'NavBar',
    methods: {
        mostrarMenu() {
            let menuMobil = document.querySelector('.navbar-links-mobile');
            let menuLeft = menuMobil.offsetLeft;

            if (menuLeft > 0) {
                menuMobil.style.left = 0;
            } else {
                menuMobil.style.left = "100vw"
            }
        },
        cerrarNavbar() {
            let menuMobil = document.querySelector('.navbar-links-mobile');
            let menuLeft = menuMobil.offsetLeft;

            if (menuLeft == 0) {
                menuMobil.style.left = "100vw";
            }
        }
    },
}
</script>