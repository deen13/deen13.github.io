<template>
  <v-bottom-navigation v-model="selection" color="primary" horizontal fixed>
    <v-btn to="/projects" nuxt height="56px">
      <span>Projekte</span>

      <v-icon>mdi-timeline-text</v-icon>
    </v-btn>

    <v-btn to="/" nuxt height="56px">
      <span>Ich</span>

      <v-icon>mdi-account</v-icon>
    </v-btn>

    <v-btn to="/content" nuxt height="56px">
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
