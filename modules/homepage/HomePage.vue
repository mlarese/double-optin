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
        color="red"> {{ $vuetify.t('To you, our warm welcome') }}</v-layout>
      <br>
      <strong> {{ $vuetify.t('We care about all the needs of our guests, especially the confidentiality') }}</strong>
      <span>{{ $vuetify.t(' For this reason, we ask you for permission to process your data according to the privacy regulations listed below ') }}</span>
      <br>
      <strong> {{ $vuetify.t(' No spam! You decide how to keep in touch with us. ') }}</strong>
      <br>
    </v-layout>
    <v-layout>
      <v-layout
        row>
        <v-flex
          xs12
          sm4
        >
          <h4>{{ $vuetify.t('Name*') }}</h4>
          <v-layout mx-1>
            <v-text-field
              :rules="rules.name"
              required
              box
              hide-details
            />
          </v-layout>

        </v-flex>

        <v-flex
          xs12
          sm4>
          <h4>{{ $vuetify.t('Surname*') }}</h4>
          <v-layout mx-1>
            <v-text-field
              :rules="surnameRules"
              :counter="10"
              required
              box
              hide-details

            />
          </v-layout>

        </v-flex>

        <v-flex
          xs12
          sm4>
          <h4 >{{ $vuetify.t('Email*') }}</h4>
          <v-layout mx-1>
            <v-text-field
              v-model="email"
              :rules="emailRules"
              type="email"
              box
              hide-details
              required
            />
          </v-layout>

        </v-flex>
        <v-flex
          xs12
          sm4>
          <h4>{{ $vuetify.t('Phone Number') }}</h4>
          <v-layout mx-1>
            <v-text-field
              v-model="phone"
              mask="phone"
              box
              hide-details
            />
          </v-layout>

        </v-flex>
      </v-layout>

    </v-layout>
    <br>
    <strong> {{ $vuetify.t(' Processing of personal data') }}</strong>
    <v-flex xs12>
      <v-textarea
        color="teal"
        box
        full-width
      />
    </v-flex>
    <v-checkbox
      v-model="checkbox"
      :rules="[(v) => !!v || 'You must agree to continue!']"
      label="You must agree to continue?"
      required
    />
    <v-checkbox
      v-model="checkbox1"
      :rules="[(v) => !!v || 'You must agree to continue!']"
      label="You must agree to continue?"
      required
    />
    <div>
      <v-layout
        justify-center
        class="my-2">
        <v-btn
          href="/thankyou"
          color="blue"
          dark
          large>
          {{ $vuetify.t('Send Your Data') }}
        </v-btn>
      </v-layout>
    </div>
  </div>
</template>
<script>
  export default {
      data () {
          return {
              rules: {
                  name: [v => !!v || this.$vuetify.t('required')]
              },
              surnameRules: [
                  (v) => !!v || 'Name is required',
                  (v) => v && v.length <= 10 || 'Name must be less than 10 characters'
              ],
              emailRules: [
                  (v) => !!v || 'E-mail is required',
                  (v) => /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
              ],
              checkbox: false,
              checkbox1: false
          }
      }
  }
</script>
