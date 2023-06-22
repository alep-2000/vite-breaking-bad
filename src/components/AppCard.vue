<script>


export default {
    props: {
        myPokemons: Object
    }
}
</script>

<template>
    <div :class="myPokemons.type1 === 'Grass' ? 'claire' : myPokemons.type1 === 'Fire' ? 'red' : myPokemons.type1 === 'Water' ? 'blue' : ''"
        class="card Kard my-2">
        <div class="d-flex justify-content-center align-items-center mt-3">
            <img :src="myPokemons.imageUrl">
        </div>
        <div class="text-center">
            <div> {{ myPokemons.code }} </div>
            <div> <strong>{{ myPokemons.name }} </strong></div>
            <div class="mb-3"> {{ myPokemons.type1 }} </div>
        </div>
    </div>
</template>

<style lang="scss">
.Kard {
    height: 240px;


    img {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        padding: 5px;
        object-fit: cover;
    }

}
</style>