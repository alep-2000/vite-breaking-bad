<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppCard from './components/AppCard.vue'
import AppSelect from './components/AppSelect.vue';
import axios from 'axios';
import { store } from './components/data/store';

export default {
  components: {
    AppHeader,
    AppMain,
    AppCard,
    AppSelect
  },
  data() {
    return {
      store
    }
  },
  mounted() {
    this.selectType()
  },
  methods: {
    selectType() {
      let myUrl = store.apiUrl

      if (store.mainType !== '') {
        myUrl += `&q[type1]=${store.mainType}`
      }


      axios.get(myUrl).then((docs) => {
        store.pokemons = docs.data.docs
      })
    },
  }
}
</script>

<template>
  <div>
    <AppSelect @select="selectType" />
    <AppHeader />
    <AppMain />
  </div>
</template>

<style lang="scss">
@use './style/generals.scss' as *;
@use './style/partials/variables' as *;
@use './style/mixins.scss' as *;
</style>
