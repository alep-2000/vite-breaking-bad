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
    }
}
</script>

<template>
    <div>
        <select v-model="store.mainType" class="form-select mt-4" @change="$emit('select', store.mainType)">
            <option value="" selected>Select type</option>
            <option v-for="(category, index) in categories" :key="index" :value="category"> {{
                category }} </option>
        </select>
    </div>
</template>

<style lang="">
    
</style>