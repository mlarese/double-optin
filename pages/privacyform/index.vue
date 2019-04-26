<template>
  <div>
    <privacy
      v-for="(booking, index) in list"
      :item="booking"
      :index="index"
      :key="index"/>
  </div>

</template>

<script>
    import {mapState} from 'vuex'
    const root = {root: true}
    import privacy from "../../components/Forms/privacy"
    export default {
        name: "Index",
        components: {privacy},
        computed: {
            ...mapState('doubleoptin', ['list']),

        },
        fetch({store}) {
            store.dispatch('doubleoptin/load', {}, root)
        }
    }
</script>

<style scoped>

</style>
