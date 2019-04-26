<template>
  <div><confirmed-email
    v-for="(guest, i) in list"
    :item="guest"
    :key="i"/>
  </div>
</template>

<script>
    import {mapState} from 'vuex'
    const root = {root: true}
    import confirmedEmail from "../../components/Email/confirmedEmail"
    export default {
        name: "ConfirmedEmail",
        components: {confirmedEmail},
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
