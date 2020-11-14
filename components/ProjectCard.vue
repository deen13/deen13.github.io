<template>
  <v-card class="mx-auto" outlined>
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

      <v-spacer></v-spacer>

      <v-btn icon @click="expanded = !expanded">
        <v-icon>{{ expanded ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>

    </v-card-actions>

    <v-expand-transition>
      <div v-show="expanded">
        <v-divider></v-divider>

        <v-list>
          <template v-for="(item, index) in value.details">
            <v-subheader v-if="item.header" :key="item.header" v-text="item.header"></v-subheader>

            <v-divider v-else-if="item.divider" :key="index" :inset="item.inset"></v-divider>

            <v-list-item v-else :key="item.title">
              <v-list-item-avatar>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-avatar>

              <v-list-item-content>
                <v-list-item-title>
                   <span class="truncate">
                  {{ item.subtitle }}
                   </span>
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </template>
        </v-list>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  props: {
    value: {
      type: Object,
      required: true
    }
  },
  data: () => ({
    expanded: false
  })
}
</script>

<style scoped>
.truncate {
  width: 250px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
