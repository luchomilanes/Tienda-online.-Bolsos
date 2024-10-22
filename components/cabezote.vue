<template>
    <div>
      <v-toolbar class="fondo"
        image="https://img.freepik.com/fotos-premium/relojes-pequenos-fotografia-alta-definicion-fondo-pantalla-creativo_993236-10125.jpg"
        dark
        height="150"
      >
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
  
        <v-toolbar-title  
        ><h1 class="title">RELOJES PRESTIGE</h1></v-toolbar-title>
  
        <v-spacer></v-spacer>
  
        <carrito class="mr-5"
         :productos="productos"
        >

        </carrito>
      </v-toolbar>
      
    </div>
  </template>
  <script>
  export default {
    props:{
      productos : Array,
    }
  }
  </script>
  <style >
  .title {
    color: #fff;
    font-family: 'Times New Roman', Times, serif;
    font-size: 2.5rem;
    text-shadow: 0px 0px  4px #fff;
  }
  .fondo {
    opacity: none;
    background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6));
     background-size: cover;
  }
   
  </style>