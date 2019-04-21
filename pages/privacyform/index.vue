<template>
  <privacy/>
</template>

<script>
    import {mapState} from 'vuex'
    const root = {root: true}
    import privacy from "../../components/Forms/privacy"
    export default {
        name: "Index",
        components: {privacy},
        computed: {
            ...mapState('clients', ['list']),

        },
        fetch({store}) {
            store.dispatch('privacy/load', {}, root)
        }
    }
</script>

<style scoped>

</style>
