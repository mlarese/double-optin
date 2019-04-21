<template>
  <greetings/>
</template>

<script>
    import {mapState} from 'vuex'
    const root = {root: true}
    import greetings from "../../components/Email/greetings"
    export default {
        name: "Index",
        components: {greetings},
        computed: {
            ...mapState('booking', ['list']),

        },
        fetch({store}) {
            store.dispatch('privacy/load', {}, root)
        }
    }
</script>

<style scoped>

</style>
