<template>
  <div id="app">
    <div id="news" class="container-fluid alert alert-dark">
       <section-api></section-api>
      </div>
  
    <div class="container-fluid">
    <div class= "row align-item-center">
    <div class="col align-item-center" v-for="(item, index) of team" :key="index">
      <team-card v-bind:member ="item"></team-card>

    </div>  
    </div>
    </div>
    
  </div>

</template>

<script>
import SectionApi from './components/SectionApi.vue'
import TeamCard from './components/TeamCard.vue'
//import datos from './team.json'

console.log('datos')

export default {
  components: { 
    SectionApi,
    TeamCard
    },
  name: 'App',
  data(){
    return{
      title : 'NOTICIAS',
      team: [{
        codigo: 1,
        nombre: "Carlos Obando",
        descripcion:
        "Profesional en áreas tecnológicas",
        rol: "Desarrollador backend",
        image:"./images/caoc.jpg",
      },
      {
        codigo: 2,
        nombre: "Jorge Andrés Mora",
        descripcion:
        "Empresario, Ingeniero Industrial, Especialista en Seguridad y Salud en el Trabajo, con experiencia en asesoria y consultoria en Gestión empresarial en normas técnicas ISO 9001, ISO 14001, ISO 45001, ISO 39001, ISO 22000 entre otras",
        rol: "Desarrollador fronted",
        image: "./images/estilo.jpg",
      },
      {
        codigo: 3,
        nombre: "Tercer Integrante",
        descripcion:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        rol: "Desarrollador frontend",
        image: "https://placeimg.com/192/192/people",
      },
      {
        codigo: 4,
        nombre: "Cuarto Integrante",
        descripcion:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        rol: "Analista",
        image: "https://placeimg.com/192/192/animals",
      },
      {
        codigo: 5,
        nombre: "Quinto Integrante",
        descripcion:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        rol: "Documentación",
        image: "https://placeimg.com/192/192/city",
      },
      ]
    }
  }
}
</script>

