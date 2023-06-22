<script>
import AppCard from '../components/AppCard.vue';
import { store } from '../store'

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
    <div class="container-md background-grey d-flex align-items-center">
        <div class="container-sm sub-container">
            <div class="row">
                <div class="col-6 col-md-2 card d-flex flex-wrap " v-for="(pokemon, index) in store.pokemons" :key="index">
                    <AppCard :myPokemons="pokemon" />
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.background-grey {
    width: 100%;
    height: 85vh;
    background-color: #DEDEDE;
    border-radius: 10px;

    .sub-container {
        width: 100%;
        height: 75vh;
        overflow-y: scroll;
        background-color: rgb(84, 89, 94);
        background: linear-gradient(90deg, rgba(84, 89, 94, 1) 54%, rgba(125, 129, 133, 1) 100%);

        .card {
            height: 240px;
            margin: 20px;

            img {
                width: 120px;
                height: 120px;
                border-radius: 50%;
                padding: 5px;
                object-fit: cover;
                background-color: white;
            }
        }
    }

}
</style>