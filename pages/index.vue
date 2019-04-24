<template>
  <div>
    <home-page/>
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
