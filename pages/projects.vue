<template>
  <v-row>
    <v-col v-for="project in projects" :key="project.title">
      <project-card :value="project"></project-card>
    </v-col>
  </v-row>
</template>


<script>
export default {
  async asyncData({$axios}) {
    const projects = await $axios.$get('https://raw.githubusercontent.com/deen13/json-store/master/projects.json')

    return {projects}
  }
}
</script>
