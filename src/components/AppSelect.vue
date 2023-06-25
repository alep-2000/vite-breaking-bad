<script>
import { store } from '../components/data/store'


export default {
    data() {
        return {
            store,
            categories: [
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water"

            ]
        }
    },

}
</script>

<template>
    <span class="d-flex justify-content-end">
        <select @change="$emit('select')" v-model="store.mainType" class="form-select-lg mt-5 me-5">
            <option value="" selected>Select type</option>
            <option v-for="(category, index) in categories" :key="index" :value="category"> {{
                category }} </option>
        </select>
    </span>
</template>

<style lang="">
    
</style>