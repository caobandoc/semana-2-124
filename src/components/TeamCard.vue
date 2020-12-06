<template>
    <div class="border border-white bg-light" style="min-height: 45rem;">
 
    <div class="alert alert-light" style="min-height: 18rem;">
        <div class= "d-flex justify-content-center p-2">
            
            <img :src="member.image" alt="Fotografía del equipo" class="rounded-circle" style="width: 12rem; max-height: 15rem;">
            
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
