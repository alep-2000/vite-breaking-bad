<script>
import AppSelect from './AppSelect.vue';
export default {
    components: { AppSelect },
    data() {
        return {
            selectType(type) {
                console.log(type)
            }
        }
    }
}
</script>

<template>
    <div class="container-md d-flex justify-content-between">
        <div class="d-flex">
            <div class="circle-blue my-3">

            </div>
            <div class="circle-red m-3">

            </div>
            <div class="circle-yellow my-3 mx-0">

            </div>
            <div class="circle-green my-3 mx-3">

            </div>
        </div>
        <div>
            <AppSelect @select="selectType" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/mixins.scss' as *;

.circle-blue {
    width: 60px;
    height: 60px;
    background-color: rgb(2, 0, 36);
    background: linear-gradient(332deg, rgba(2, 0, 36, 1) 0%, rgba(9, 9, 121, 1) 30%, rgba(255, 255, 255, 1) 100%);
    border-radius: 50%;
    border: 3px solid white;
}

.circle-red {
    @include circle;
    background-color: rgb(0, 35, 100);
    background: linear-gradient(332deg, rgba(2, 0, 36, 1) 0%, rgba(242, 43, 13, 1) 30%, rgba(255, 255, 255, 1) 100%);
}

.circle-yellow {
    @include circle;
    background-color: rgb(0, 100, 100);
    background: linear-gradient(332deg, rgba(2, 0, 36, 1) 0%, rgba(241, 222, 4, 1) 30%, rgba(255, 255, 255, 1) 100%);
}

.circle-green {
    @include circle;
    background-color: rgb(0, 100, 100);
    background: linear-gradient(332deg, rgba(2, 0, 36, 1) 0%, rgba(61, 161, 64, 1) 30%, rgba(255, 255, 255, 1) 100%);
}
</style>