<template>
  <v-select
    :items="items"
    v-model="model"
    label="Quem"
    autocomplete
    >
  </v-select>
</template>

<script>
  export default {
    name: 'who-payment',
    props: ['model', 'items']
  }
</script>
