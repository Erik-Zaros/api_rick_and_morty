<script setup>
const character = defineProps(["name", "url", "status", "species", "gender", "location", "episode"])
const characterId = character.url.split('/')[5]
const imageUrl= "https://rickandmortyapi.com/api/character/avatar/" + characterId + ".jpeg"
console.log(imageUrl)

</script>

<template>  
    <div class="col-md-3">
        <div class="card p-2 mb-1">
            <img :src="imageUrl" height="300" alt="">
            <p class="text-center"><b>Nome:</b> {{character.name}}</p>
            <p class="text-center"><b>Status:</b> {{character.status}}</p>
            <p class="text-center"><b>Espécie:</b> {{character.species}}</p>
            <p class="text-center"><b>Gênero:</b> {{character.gender}}</p>
            <p class="text-center"><b>Localização Atual:</b> {{character.location.name}}</p>
            <p class="text-center"><b>Quantidade de Episódios que Apareceu:</b> {{character.episode.length}}</p>
        </div>
    </div>
</template>
