<script>
export default {

}
</script>

<template>
    <div>
        <select @change="$emit(selectValue)" value="" class="form-select mt-4">
            <option value="" selected>Choose status </option>
            <option value="Electric">Electric</option>
            <option value="Grass">Grass</option>
            <option value="Water">Water</option>
        </select>
    </div>
</template>

<style lang="">
    
</style>