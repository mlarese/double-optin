<template>
  <div>
    <home-page
      v-for="(guest, i) in list"
      :item="guest"
      :key="i"
    />
  </div>
</template>

<script>
    import {mapState} from 'vuex'
    import HomePage from '../modules/homepage/HomePage'
    const root = {root: true}
    export default {
        components: {HomePage},
        computed: {
            ...mapState('privacy', ['list']),

        },
        fetch({store}) {
            store.dispatch('privacy/load', {}, root)
        }
    }
</script>

<style scoped>

</style>
