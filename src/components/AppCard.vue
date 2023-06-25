<script>
import { store } from '../components/data/store';

export default {
    data() {
        return {
            store,
            colorMap: {
                "Bug": 'rgb(163, 231, 99)',
                "Dark": 'rgb(77, 77, 77)',
                "Dragon": 'rgb(117,93,225)',
                "Electric": 'rgb(255, 255, 0)',
                "Fairy": 'rgb(255, 192, 203)',
                "Fighting": 'rgb(158, 76, 76)',
                "Fire": 'rgb(255, 0, 0)',
                "Flying": 'rgb(173, 216, 230)',
                "Ghost": 'rgb(100, 0, 150)',
                "Grass": 'rgb(76, 158, 76)',
                "Ground": 'rgb(158, 123, 9)',
                "Ice": 'rgb(106, 186, 212)',
                "Normal": 'rgb(190, 190, 190)',
                "Poison": 'rgb(128, 0, 128)',
                "Psychic": 'rgb(201, 0, 184)',
                "Rock": 'rgb(100, 50, 50)',
                "Steel": 'rgb(148, 148, 148)',
                "Water": 'rgb(0, 0, 255)'
            }
        }
    },
    props: {
        myPokemons: Object,
        mainType: String,
    },
    computed: {
        upperName() {
            return this.myPokemons.name.toUpperCase();
        }
    }
}
</script>

<template>
    <div class="card my-2"
        :class="myPokemons.type1 === 'Grass' ? 'grass_back' : myPokemons.type1 === 'Fire' ? 'fire_back' : myPokemons.type1 === 'Water' ? 'water_back' : myPokemons.type1 === 'Bug' ? 'bug_back' : myPokemons.type1 === 'Dark' ? 'dark_back' : myPokemons.type1 === 'Dragon' ? 'dragon_back' : myPokemons.type1 === 'Electric' ? 'electric_back' : myPokemons.type1 === 'Fairy' ? 'fairy_back' : myPokemons.type1 === 'Fighting' ? 'fighting_back' : myPokemons.type1 === 'Flying' ? 'flying_back' : myPokemons.type1 === 'Ghost' ? 'ghost_back' : myPokemons.type1 === 'Ground' ? 'ground_back' : myPokemons.type1 === 'Ice' ? 'ice_back' : myPokemons.type1 === 'Normal' ? 'normal_back' : myPokemons.type1 === 'Poison' ? 'poison_back' : myPokemons.type1 === 'Psychic' ? 'psychic_back' : myPokemons.type1 === 'Rock' ? 'rock_back' : myPokemons.type1 === 'Steel' ? 'steel_back' : ''">
        <div class="d-flex justify-content-center align-items-center mt-3">
            <img :src="myPokemons.imageUrl">
        </div>
        <div class="text-center">
            <div> {{ myPokemons.code }} </div>
            <div> <strong>{{ upperName }} </strong></div>
            <div class="mb-3"> {{ myPokemons.type1 }} </div>
        </div>
    </div>
</template>

<style lang="scss">
img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    padding: 5px;
    object-fit: cover;
}
</style>