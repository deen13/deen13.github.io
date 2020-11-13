<template>
  <v-btn v-if="$nuxt.$route.path !== path" x-large dark nuxt :to="path" class="mx-2">
    {{ label }}
  </v-btn>
</template>

<script>
export default {
  props: {
    path: {
      type: String,
      required: true
    },
    label: {
      type: String,
      required: true
    }
  }
}
</script>
