<template>
    <div class="border border-white bg-light">
 
    <div class="alert alert-light">
        <div class= "d-flex justify-content-center p-2">
            <span class="border border-dark">
            <img :src="member.image" alt="Fotografía del equipo" class="rounded-lg">
            </span>
        </div>
         </div>
        <div class=text-center>
            <div class="card text-white bg-dark mb-2" style="max-width: 50rem;">
            <h4 class="card-title">{{member.nombre}}</h4>
        </div>
        
            <ul class="card-body">
                <li>{{member.descripcion}}</li>
                <li><span> Rol: </span>{{member.rol}}</li>
            </ul>
     </div>
   
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
