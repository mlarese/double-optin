<template>
  <v-container row>
    <div><h2> name  surname : {{ $vuetify.t('here are your subscriptions to the regulations of the website www.miodominio.com') }}</h2></div>
    <v-layout class="align-baseline"> <span>{{ $vuetify.t('If you wish you can modify') }}</span>
      <v-spacer/>
      <v-btn
        color="blue"
        dark>{{ $vuetify.t('revokes all the concenses') }}
      </v-btn>
    </v-layout>
    <hr class="my-2">
    <v-layout>
      <h3>{{ $vuetify.t('Regulations') }}: No1_Privacy </h3>
    </v-layout>
    <v-layout><span>{{ $vuetify.t('Website origin') }}: httml//www.courage.com</span></v-layout>
    <br>
    <v-layout>
      <span style="color: cadetblue;">
        {{ $vuetify.t('Last update: ' ) }}  dd/mm/yyyy {{ $vuetify.t('at ' ) }}  hh/mm/ss {{ $vuetify.t('from IP Address: ' ) }} 00:1123:32:54
      </span>
      <v-spacer/>
      <strong>{{ $vuetify.t( '*mandatory fields' ) }}</strong>
    </v-layout>
    <br>
    <v-layout
      row>
      <v-flex
        xs12
        sm4>
        <h4>{{ $vuetify.t('Name*') }}</h4>
        <v-layout mx-1>
          <v-text-field
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
            :counter="10"
            box
            hide-details/>
        </v-layout>
      </v-flex>
      <v-flex
        xs12
        sm4>
        <h4 >{{ $vuetify.t('Email*') }}</h4>
        <v-layout mx-1>
          <v-text-field
            type="email"
            box
            hide-details
          />
        </v-layout>
      </v-flex>
      <v-flex
        xs12
        sm4>
        <h4>{{ $vuetify.t('Phone Number*') }}</h4>
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
    <br>
    <v-layout row>
      <v-flex
        xs12
        sm3>
        <h4>{{ $vuetify.t('Others') }}</h4>
        <v-layout mx-1>
          <v-text-field
            box
            hide-details
          />
        </v-layout>
      </v-flex>
      <v-flex
        xs12
        sm3>
        <h4>{{ $vuetify.t('Others') }}</h4>
        <v-layout mx-1>
          <v-text-field
            :counter="10"
            box
            hide-details/>
        </v-layout>
      </v-flex>
    </v-layout>
    <br>
    <v-layout row>
      <v-flex
        xs12
        sm12>
        <h4>{{ $vuetify.t('Message*') }}</h4>
        <v-layout mx-1>
          <v-text-field
            box
            hide-details
          />
        </v-layout>
      </v-flex>
    </v-layout>
    <br>
    <strong> {{ $vuetify.t(' Processing of personal data*') }}</strong>
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
    <br>
    <strong> {{ $vuetify.t(' Processing of personal data*') }}</strong>
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
    <v-layout >
      <v-spacer/>
      <v-btn
        dark
        color="blue-grey"
      >{{ $vuetify.t('send') }}
        <v-icon
          right
          dark>arrow_forward</v-icon>
      </v-btn>

    </v-layout>
  </v-container>
</template>

<script>
    export default {
        name: "Privacy"
    }
</script>

<style scoped>

</style>
