<template>
  <div>
    <v-subheader>Projects</v-subheader>
    <v-container class="my-5">
      <v-expansion-panels>
        <v-expansion-panel v-for="project in myProjects" :key="project.title">
          <v-expansion-panel-header>
            {{ project.title }}
          </v-expansion-panel-header>
          <v-expansion-panel-content class="px-4 grey--text">
            <div class="font-weight-bold">
              due by {{ project.due }}
            </div>
            <p>{{ project.content }}</p>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-container>
  </div>
</template>

<script>
import Content from '../assets/mock/projects'

export default {
  name: 'projects',
  data() {
    return {
      projects: Content.projects
    }
  },
  computed: {
    myProjects () {
      return this.projects.filter(item => item.person === 'Carlos Wimmer')
    }
  }
}
</script>
