<template>
  <div>
    <greetings
      v-for="(booking, index) in list"
      :item="booking"
      :index="index"
      :key="index"/>
  </div>
</template>

<script>
    import {mapState} from 'vuex'
    const root = {root: true}
    import greetings from "../../components/Email/greetings"
    export default {
        name: "Index",
        components: {greetings},
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
