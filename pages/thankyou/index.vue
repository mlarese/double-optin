<template>
  <div>
    <v-layout
      column
      justify-center
      align-center
    >
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
      <v-layout
        class="title"
        color="red"> {{ $vuetify.t('Thank You') }} {{ Mauro }}!</v-layout>
      <br>
      <span>{{ $vuetify.t(' We sent you an email. ') }}</span>

      <strong> {{ $vuetify.t(' PLease, answer to confirm your personal details ') }}</strong>
    </v-layout>
    <v-layout
      column
      justify-center
      align-center
    >
      <v-flex
        xs5
        sm5
        md5>
        <v-icon
          slot="activator"
          size="100px"
          class="my-5"
          color="blue"
        >
          email
        </v-icon>
      </v-flex>
    </v-layout>
    <div>
      <v-layout
        justify-center
        class="my-2">
        <v-btn
          href="/confirmationemail"
          flat
          large>{{ $vuetify.t('Return to HomePage') }}
        </v-btn>
      </v-layout>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Index"
    }
</script>

<style scoped>

</style>
