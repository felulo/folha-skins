<template>
  <v-layout
    row
    wrap
    >
    <v-flex xs12>
      <item-payment 
        :itemPayment="itemPayment"
        :personsPayment="personsPayment"
        >
      </item-payment>
    </v-flex>

    <v-flex
      xs12
      class="text-xs-right"
      >
      <v-btn
        error
        light
        >
        Limpar
      </v-btn>
      <v-btn
        primary
        light
        >
        Incluir
      </v-btn>
    </v-flex>
  </v-layout>
</template>

<script>
  import ItemPayment from './itemPayment.vue';

  export default {
    name: 'payment-form',
    props: ['itemPayment', 'personsPayment'],
    components: {
      ItemPayment
    }
  }
</script>
