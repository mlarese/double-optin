<template>
  <v-layout row>
    <div><h2>{{ name }} {{ surname }}: {{ $vuetify.t('here are your subscriptions to the regulations of the website www.miodominio.com') }}</h2></div>
    <v-layout row> <span>{{ $vuetify.t('if you wish you can modify') }}</span>
      <v-spacer/>
      <v-btn
        color="blue"
        dark
        large>{{ $vuetify.t('revokes all the concenses') }}
      </v-btn>
    </v-layout>
    <hr class="my-4">
    <v-layout>
      <span>{{ $vuetify.t('Regulations') }}: {{ N01_privacy }}</span>
    </v-layout>
    <v-layout><span>{{ $vuetify.t('Website origin') }}: {{ courage.com }}</span></v-layout>
  </v-layout>
</template>

<script>
    export default {
        name: "Privacy"
    }
</script>

<style scoped>

</style>
