<script>
import axios from 'axios'

    export default {
        data() {
            return {
                pokemonData: null,

            }
        },
        //lifecycle (option or composition api)
        created() {
            axios.get('https://pokeapi.co/api/v2/pokemon/umbreon').then((result) => {
                this.pokemonData = result.data
            })
        }

    }
</script>


<template>
    <div>
        <div v-if="pokemonData">
            <h2>{{ pokemonData.name }}</h2>
            <img class="imgPokemon" :src="pokemonData.sprites.other.dream_world.front_default" alt="Pokemon image">
            <img class="imgPokemon" :src="pokemonData.sprites.other.home.front_default" alt="Pokemon image">
            <img class="imgPokemon" :src="pokemonData.sprites.other.home.front_shiny" alt="Pokemon image">
            <h3>HP: {{ pokemonData.stats[0].base_stat }}</h3>
            <h3>Attack: {{ pokemonData.stats[1].base_stat }}</h3>
            <h3>Defense: {{ pokemonData.stats[2].base_stat }}</h3>
            <h3>Speed: {{ pokemonData.stats[3].base_stat }}</h3>
        </div>
    </div>
</template>

<style lang="css" scoped>
    .imgPokemon {
        width: 200px;
    }
</style>


