<template>
  <div>

    <v-layout
      column
      justify-center
      align-center
    >

      <v-card class="elevation-0">
        <v-flex
          xs5
          sm5
          md5>
          <v-avatar
            slot="activator"
            size="100px"
            class="my-5"
          >
            <img

              src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460"
              alt="Avatar"
            >
          </v-avatar>
        </v-flex>
        <v-card-title class="headline">


          {{ $vuetify.t('Gentile') }} {{ user }} </v-card-title>
        <v-card-text>
          <span class="my-4"> {{ $vuetify.t('To facilitate you on arrival at our facility,') }}</span>
          <br>
          <span > {{ $vuetify.t('click the button below') }} </span>
          <br>
          <v-layout
            justify-center
            class="my-2">
            <v-btn
              href="/precheckin"
              color="blue"
              dark
              large>{{ $vuetify.t('Confirm Your Data') }}</v-btn>

          </v-layout><v-layout
            justify-center
            color="blue"
            class="my-2">
            <a

              href="/"
            >{{ $vuetify.t ('If you do not see the button correctly, click here' )
            }}</a>

          </v-layout>
          <span class="my-2">{{ $vuetify.t ('If you do not effect the Pre Check-in your booking is still valid, you can still') }} </span>
          <br>
          <span>{{ $vuetify.t ('do it when you arrive at the facility.') }}</span>
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
