<template>
  <v-layout row wrap>
    <v-flex xs12>
      <v-text-field
        label="Pra que"
        v-model="itemPayment.value"
        >
      </v-text-field>
    </v-flex>

    <v-flex xs6>
      <who-payment 
        :model="itemPayment.whoPayment"
        :items="personsPayment"
        >
      </who-payment>
    </v-flex>

    <v-flex xs6>
      <v-text-field
        label="Valor"
        v-model="itemPayment.value"
        >
      </v-text-field>
    </v-flex>

    <v-flex xs12>
      <who-will-payment 
        :model="itemPayment.whoWillPayment"
        :items="personsPayment"
        >
      </who-will-payment>
    </v-flex>
  </v-layout>
</template>

<script>
  import WhoPayment from './whoPayment.vue';
  import WhoWillPayment from './whoWillPayment.vue';

  export default {
    components: {
      WhoPayment,
      WhoWillPayment
    },
    name: 'item-payment',
    props: ['itemPayment', 'personsPayment'],
  }
</script>