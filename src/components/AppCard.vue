<script>


export default {
    props: {
        myPokemons: Object
    }
}
</script>

<template>
    <div class="d-flex justify-content-center align-items-center mt-3">
        <img :src="myPokemons.imageUrl">
    </div>
    <div class="text-center">
        <div> {{ myPokemons.code }} </div>
        <div> <strong>{{ myPokemons.name }} </strong></div>
        <div> {{ myPokemons.type1 }} </div>
    </div>
</template>

<style lang="scss"></style>