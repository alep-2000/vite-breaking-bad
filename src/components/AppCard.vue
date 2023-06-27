<script>
import { store } from '../components/data/store';
import { colorMap } from '../components/data/index';

export default {
    data() {
        return {
            store,
            colorMap
        }
    },
    props: {
        myPokemons: Object,
        mainType: String,
    },
    computed: {
        upperName() {
            return this.myPokemons.name.toUpperCase();
        },
        backColor() {
            return colorMap[store.mainType];
        }
    }
}
</script>

<template>
    <div class="card my-2"
        :class="myPokemons.type1 === 'Grass' ? 'grass_back' : myPokemons.type1 === 'Fire' ? 'fire_back' : myPokemons.type1 === 'Water' ? 'water_back' : ''"
        :style="`background-color: ${backColor}`">
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