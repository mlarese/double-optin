<template>
  <v-container>
    <v-layout
      column
      justify-center
      align-center>
      <v-flex
        xs5
        sm5
        md5>
        <v-avatar
          slot="activator"
          size="100px"
          class="my-5">
          <img
            src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460"
            alt="Avatar">
        </v-avatar>
      </v-flex>
      <v-layout class="justify-center"> <h1>{{ $vuetify.t('Done!') }}</h1></v-layout>
      <br>
      <v-layout
        column
        justify-center
        align-center>
        <v-icon
          slot="activator"
          size="50px"
          color="blue">
          thumb_up_alt
        </v-icon>
      </v-layout>
      <v-layout
        justify-center
        align-center><strong class="align-center"> {{ $vuetify.t('Your data as been confirm.') }}</strong></v-layout>
      <br>
      <v-layout
        justify-center
        align-center><span > {{ $vuetify.t('we take orders only from you') }} </span></v-layout>
      <v-layout
        justify-center
        align-center><span > {{ $vuetify.t('on your indications,') }} </span></v-layout>
      <br>
      <v-layout class="justify-center"> <h3>{{ $vuetify.t('Thank You!') }}</h3></v-layout>
      <br>
      <v-layout class="justify-center"> <span>{{ $vuetify.t('Do you want to view or edit your details?') }}</span></v-layout>
      <br>
      <v-layout
        justify-center
        class="my-2">
        <v-btn
          href="/privacyform"
          color="blue"
          dark
          large>{{ $vuetify.t('View the summary') }}</v-btn>

      </v-layout>
    </v-layout>
  </v-container>
</template>

<script>
    export default {
        name: "ConfirmedEmail"
    }
</script>

<style scoped>

</style>
