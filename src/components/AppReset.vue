<script>
import { store } from './data/store';

export default {
    data() {
        return {

        }
    },
    methods: {
        reset() {
            store.mainType = '';

            this.$emit('select')
        }
    }
}
</script>

<template>
    <div>
        <button class="btn btn-md btn-warning mt-5 me-3" @click="reset">Cancella</button>
    </div>
</template>

<style lang="">
    
</style>