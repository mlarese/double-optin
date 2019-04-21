<template>
  <confirmation-email/>
</template>

<script>
    import {mapState} from 'vuex'
    const root = {root: true}
    import confirmationEmail from "../../components/Email/confirmationEmail"
    export default {
        name: "Index",
        components: {confirmationEmail},
        computed: {
            ...mapState('booking', ['list']),

        },
        fetch({store}) {
            store.dispatch('booking/load', {}, root)
        }
    }
</script>

<style scoped>

</style>
