<template>
  <v-app light>
    <v-toolbar fixed>
      <v-toolbar-title>
        Folha Pagamento Skins
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>
          person_add
        </v-icon>
      </v-btn>
    </v-toolbar>
    <main>
      <v-container grid-list-md>
        <v-layout
          row
          wrap
          >
          <v-flex xs6>
            <payment-form
              :itemPayment="itemPayment"
              :personsPayment="personsPayment"
              >
            </payment-form>
          </v-flex>
        </v-layout>
      </v-container>
    </main>
  </v-app>
</template>

<script>
  import PaymentForm from './components/paymentForm/paymentForm.vue';

  export default {
    components: {
      PaymentForm
    },
    data() {
      return {
        itemPayment: {},
        personsPayment: [],
        items: []
      }
    }
  }
</script>
