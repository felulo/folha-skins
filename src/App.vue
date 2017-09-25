<template>
  <v-app light>
    <v-toolbar fixed>
      <v-toolbar-title>
        Folha Pagamento Skins
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn 
        icon
        @click.native.stop="openPersonDialog()">
        <v-icon>
          person_add
        </v-icon>
      </v-btn>

      <people-dialog
        :open-dialog="personDialogOpened"
        :persons="personsPayment">
      </people-dialog>
    </v-toolbar>
    <main>
      <v-container grid-list-md>
        <v-layout
          row
          wrap
          >
          <v-flex md6>
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
  import PeopleDialog from './components/peopleDialog/peopleDialog.vue';

  export default {
    components: {
      PaymentForm,
      PeopleDialog
    },
    data() {
      return {
        itemPayment: {},
        personsPayment: [],
        items: [],
        personDialogOpened: false
      }
    },
    methods: {
      openPersonDialog() {
        this.personDialogOpened = true;
      }
    }
  }
</script>
