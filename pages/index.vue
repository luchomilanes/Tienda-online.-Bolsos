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
         <span>&copy; 2024 Relojes Prestige. Todos los derechos reservados.</span>
<br>
<span>Explora nuestra colección de relojes de lujo, deportivos y clásicos. Perfectos para cualquier ocasión, combinando precisión y estilo.</span>
<br>
<span>Contacto: soporte@relojesprestige.com | Tel: +1 800 987 6543</span>
<br>
<span>Síguenos en redes sociales: Facebook, Instagram, Twitter</span>

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
               imagen : 'https://down-co.img.susercontent.com/file/sg-11134301-7rdyr-lybzu3r5yybn43@resize_w450_nl.webp',
               precio :  13.300,
               titulo : ' Reloj Electrónico',
               descripcion : 'Nueva Moda Led Reloj Electrónico Estudiante Reloj Electrónico Hombres Mujeres Accesorios Reloj'
           },
            {
               imagen : 'https://down-co.img.susercontent.com/file/sg-11134201-7rdx5-lykba5cdk4cnc9@resize_w450_nl.webp',
               precio : 14.369,
               titulo : 'Reloj De Moda Cuarzo',
               descripcion : 'Reloj De Moda Cuarzo Con Correa De Malla De Luz Nocturna Ultrafina Y Minimalista',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/cn-11134207-7r98o-luli4zbn38hs9b@resize_w450_nl.webp',
               precio : 20.987,
               titulo : 'Reloj Paw Patrol',
               descripcion : 'Socute Paw Patrol Proyección Reloj Chase Marshall Rubble Skye Cubierta Abatible',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/sg-11134301-7rdvy-lxfnf66q3s5kcc@resize_w450_nl.webp',
               precio : 14.255,
               titulo : 'Reloj Malaquita Verde Diamante',
               descripcion : 'Moda Versión Coreana Popular Rectangular Señoras Cinturón Reloj Malaquita Verde Diamante Mujer Estudiante Reloj De Cuarzo',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/72d7949da51d4ef087d260526e61ddcb@resize_w450_nl.webp',
               precio : 26.399,
               titulo : 'Reloj de cuarzo/ minimalista',
               descripcion : 'Los hombres de la moda Simple de agua fantasma relojes/alta calidad de acero inoxidable correa de malla',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/sg-11134301-7rdyx-lxdqnkhaxgnz49@resize_w450_nl.webp',
               precio : 24.551,
               titulo : 'Reloj Electrónico Influencer ',
               descripcion : 'Reloj Multifuncional Al Aire Libre Retro Luminoso Deportes Reloj Electrónico Influencer Adulto Estudiante Reloj Hombres Gran Dial',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/717f13f9ab740672a1eb3012016b81b4@resize_w450_nl.webp',
               precio : 12.000,
               titulo : 'Reloj De Cuarzo Con Banda De Acero ',
               descripcion : 'Inoxidable Multi Color Opcional A La Moda Para Mujer reloj',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/sg-11134301-7rdx4-m00b1bb9u0on76@resize_w450_nl.webp',
               precio : 13.656,
               titulo : 'Reloj De Las Mujeres Nueva Moda',
               descripcion : 'Simple pulsera correa',

            } ,
            {
               imagen : 'https://down-co.img.susercontent.com/file/sg-11134201-7qvd5-lhuq0nu5se3p0f@resize_w450_nl.webp',
               precio : 28.129,
               titulo : 'Reloj electrónico cuadrado ',
               descripcion : 'mejorado Y1 reloj electrónico LED con botón deportivo para estudiantes y niños|',

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