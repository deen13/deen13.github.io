<template>
  <v-bottom-navigation v-model="selection" color="primary" horizontal fixed>
    <v-btn to="/projects" nuxt>
      <span>Projekte</span>

      <v-icon>mdi-timeline-text</v-icon>
    </v-btn>

    <v-btn to="/" nuxt>
      <span>Ich</span>

      <v-icon>mdi-account</v-icon>
    </v-btn>

    <v-btn to="/content" nuxt>
      <span>Content</span>

      <v-icon>mdi-post</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
export default {
  data: () => ({ selection: 1 }),
}
</script>
