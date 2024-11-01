<template>
   <div>
       <cabezote
        :productos="comprasrealizadas"
       ></cabezote>

       <manager
        :productos="productos"
        @compra="compra">
       </manager>
       <footer class="pie">
         <span>&copy; 2024 Bagify. Todos los derechos reservados.</span>
<br>
<span>Descubre nuestra colección de bolsos de moda, elegantes y funcionales. Diseñados para cada estilo y ocasión, combinando calidad y tendencia.</span>
<br>
<span>Contacto: soporte@bagify.com | Tel: +1 800 123 4567</span>
<br>
<span>Síguenos en redes sociales: Facebook, Instagram, Pinterest</span>

       </footer>
   </div>
</template>
<script>
import cabezote from '~/components/cabezote.vue'
export default {
 components: { cabezote },
   data() {
       return {
        
         comprasrealizadas : [],
         productos : [
           {
               imagen : 'https://down-co.img.susercontent.com/file/4fed68df9deb9807d113e45497f28a72.webp',
               precio : 28.434,
               titulo : ' Mini bolsos de la eslinga',
               descripcion : ' las mujeres Mini bolsos de la eslinga de la cadena bolso de hombro bolsos bolsos de mensajero'
           },
            {
               imagen : 'https://down-co.img.susercontent.com/file/afd92fbd9a3a405afd94e672d30a29df.webp',
               precio : 46.800,
               titulo : 'mujer moda casual',
               descripcion : 'gran capacidad retro letra impresión cremallera bolsos',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/e4190d3b4194c99f9cde9c90d6b169d6.webp',
               precio : 57.000,
               titulo : ' bolsa de Nylon ',
               descripcion : 'Nueva bolsa de Nylon de lona para mujer Crossbody de un solo hombro ligero multicapa Casual bolso de las señoras',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/f571e88587f8e3672f7b8f0c0bb481d3.webp',
               precio : 25.412,
               titulo : 'Bolso de viaje ',
               descripcion : 'plegable impermeable bolso de viaje maleta bolsa de almacenamiento de gran capacidad bolsas de hombro',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/8a5f2b9d91ec8367899452460a09487a.webp',
               precio : 83.999,
               titulo : 'Bolso de hombro bandolera',
               descripcion : '2021 nuevo bolso de hombro bandolera bolso de moda de las mujeres coreano nuevo pequeño bolso',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/5b5817b7738509ad0763ac5ceb157eef.webp',
               precio : 146.509,
               titulo : 'Mochila escolar  ',
               descripcion : 'Mochila escolar de Color degradado para niña, morral escolar de princesa arcoíris, bolso de gran capacidad para fin de semana',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/6401aba68b69572d5e64311d0467e152.webp',
               precio : 72.456,
               titulo : 'Mochila Coreana ',
               descripcion : 'Coreana 2021 nueva marea salvaje sin costuras De cuero suave impermeable bolso De escuela Mochila De viaje De gran',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/sg-11134201-7qvfs-ljr4t5cfzk7mc8.webp',
               precio :84.114,
               titulo : 'Bolso de mensajero ',
               descripcion : 'Bolso de mensajero trapstar bolso bandolera de hombro para hombres y mujeres',

            

            } ,

         ]
           

                              
          
       }
   },
   methods: {
     compra(data){
        this.comprasrealizadas.push(data)
     }
   },
}
</script>
<style>
.pie {
   background-color: #333; /* Color de fondo oscuro */
  color: #fff; /* Color del texto blanco */
  padding: 20px 0; /* Espaciado */
  text-align: center; /* Centrar el texto */
}
.pie span {
   font-size: 14px; /* Tamaño de fuente */
   opacity: 0.8; /* Opacidad para hacer el texto menos brillante */
}
</style>