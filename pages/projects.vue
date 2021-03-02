<template>
    <v-row>
        <v-col v-for="project in projects" :key="project.title" cols="12">
            <project-card :value="project"></project-card>
        </v-col>
    </v-row>
</template>

<script>
  export default {
    async asyncData({ $axios }) {
      const response = await $axios.$get('projects.json')

      return { projects: JSON.parse(new Buffer(response.content, 'base64').toString()) }
    }
  }
</script>
