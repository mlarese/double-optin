<template>
  <div>
    <v-layout
      justify-center
      align-center
    >

      <v-card class="elevation-0">
        <v-layout
          column
          justify-center
          align-center>
          <v-avatar
            size="100px"
            class="my-5"
          ><img
            src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460"
            alt="Avatar"
          >
          </v-avatar>
        </v-layout>


        <v-layout class="justify-center"> <h1>{{ $vuetify.t('Done!') }}</h1></v-layout>
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
        <v-card-text>
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
              href="/"
              color="blue"
              dark
              large>{{ $vuetify.t('View the summary') }}</v-btn>

          </v-layout>
        </v-card-text>
      </v-card>
    </v-layout>
  </div>
</template>

<script>
    export default {
        name: "Index"
    }
</script>

<style scoped>

</style>
