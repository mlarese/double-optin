<template>
  <div>
    <confirmation-email
      v-for="(guest, i) in list"
      :item="guest"
      :key="i"/>
  </div>
</template>

<script>
    import {mapState} from 'vuex'
    const root = {root: true}
    import confirmationEmail from "../../components/Email/confirmationEmail"
    export default {
        name: "Index",
        components: {confirmationEmail},
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
