<script>
import { store } from '../components/data/store';

export default {
    data() {
        return {
            store
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
    <!-- <div :class="myPokemons.type1 === 'Grass' ? 'claire' : myPokemons.type1 === 'Fire' ? 'red' : myPokemons.type1 === 'Water' ? 'blue' : ''" -->
    <div class="card my-2">
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