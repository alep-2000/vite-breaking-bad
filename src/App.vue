<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppCard from './components/AppCard.vue'


export default {
  components: {
    AppHeader,
    AppMain,
    AppCard
  }
}
</script>

<template>
  <div>
    <AppHeader />
    <AppMain />

  </div>
</template>

<style lang="scss">
@use './style/generals.scss' as *;
@use './style/partials/variables' as *;
@use './style/mixins.scss' as *;
</style>
