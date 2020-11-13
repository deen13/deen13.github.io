<template>
  <v-row>
    <v-col v-for="project in projects" :key="project.title" cols="12">
      <project-card :value="project"></project-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  layout: (ctx) => ctx.isMobile ? 'mobile' : 'desktop',
  async asyncData({$axios}) {
    const projects = await $axios.$get('projects.json')

    return {projects}
  }
}
</script>
