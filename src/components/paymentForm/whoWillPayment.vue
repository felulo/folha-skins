<template>
  <v-select
    v-model="model"
    label="Para quem"
    chips
    tags
    :items="items"
    >
    <template
      slot="selection"
      scope="data"
      >
      <v-chip
        class="chip--select-multi"
        :selected="data.selected"
        :disabled="data.disabled"
        :key="JSON.stringify(data.item)"
        @input="data.parent.selectItem(data.item)"
        >
        <v-avatar class="accent">
          {{ data.item.slice(0, 1).toUpperCase() }}
        </v-avatar>
        {{ data.item }}
      </v-chip>
    </template>
  </v-select>
</template>

<script>
  export default {
    name: 'who-will-payment',
    props: ['model', 'items']
  }
</script>

