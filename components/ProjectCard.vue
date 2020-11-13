<template>
  <v-card class="mx-auto" max-width="344" outlined>
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-subtitle>{{ value.company }} • {{ value.year }}</v-list-item-subtitle>
        <v-list-item-title class="headline mb-1">
          {{ value.title }}
        </v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-card-text class="py-0">
      {{ value.description }}
    </v-card-text>

    <v-card-actions>
      <v-chip-group column>
        <v-chip v-for="tag in value.tags">{{ tag }}</v-chip>
      </v-chip-group>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    value: {
      type: Object,
      required: true
    }
  }
}
</script>
