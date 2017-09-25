<template>
  <v-layout
    row
    justify-center
    >
    <v-dialog
      v-model="openDialog"
      width="50%">
      <v-card>
        <v-card-title class="headline">
          Pessoas
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              <v-flex xs12>
                <v-text-field
                  label="Nome"
                  v-model="personName"
                  :append-icon="'add'"
                  :append-icon-cb="() => { this.addPerson() }">
                </v-text-field>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card-text>
      </v-card>
    </v-dialog>
  </v-layout>
</template>

<script>
  import voca from 'voca';

  export default {
    name: 'people-dialog',
    props: ['openDialog', 'persons'],
    data() {
      return {
        personName: ''
      };
    },
    methods: {
      addPerson() {
        let persons = this.persons;
        let personWillAdd = voca.titleCase(this.personName);

        if (!persons.includes(personWillAdd)) {
          persons.push(personWillAdd);

          this.personName = '';
        }
      }
    }
  }
</script>