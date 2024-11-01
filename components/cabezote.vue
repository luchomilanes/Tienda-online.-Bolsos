<template>
    <div>
      <v-toolbar class="fondo"
        image="https://png.pngtree.com/background/20230524/original/pngtree-group-of-different-colored-handbags-picture-image_2707306.jpg"
        dark
        height="150"
      >
        <v-app-bar-nav-icon class="menu"></v-app-bar-nav-icon>
  
        <v-toolbar-title  
        ><h1 class="title">BAGIFY</h1></v-toolbar-title>
  
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
    font-family:monospace;
    font-size: 2.5rem;
    text-shadow: 0px 0px  4px #fff;
    letter-spacing: 4px
  }
  .fondo {
    opacity: none;
    background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6));
     background-size: cover;
  }
  .menu {
    color: #fff;
  }
   
  </style>