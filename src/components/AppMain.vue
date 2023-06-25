<script>
import AppCard from '../components/AppCard.vue';
import { store } from '../components/data/store'

export default {
    components: {
        AppCard
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container background-grey rounded-4 p-4 d-flex align-items-center">
        <div class="container-sm sub-container">
            <div class="row">
                <div class=" col-6 col-md-4 col-lg-3" v-for="(pokemon, index) in store.pokemons  " :key="index">
                    <AppCard :myPokemons="pokemon" />
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.background-grey {
    background-color: #DEDEDE;


    .sub-container {
        width: 100%;
        height: 45vh;
        overflow-y: scroll;
        background-color: rgb(84, 89, 94);
        background: linear-gradient(90deg, rgba(84, 89, 94, 1) 54%, rgba(125, 129, 133, 1) 100%);
    }

}
</style>