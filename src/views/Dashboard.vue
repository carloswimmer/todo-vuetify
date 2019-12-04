<template>
  <div>
    <v-subheader>Dashboard</v-subheader>
    <v-container class="my-5">
      <v-row class="mb-3">
        <v-btn small text color="grey" class="mx-3" @click="sortBy('title')">
          <v-icon left>mdi-folder</v-icon>
          <span class="caption text-lowercase">by project</span>
        </v-btn>
        <v-btn small text color="grey" class="mx-3" @click="sortBy('person')">
          <v-icon left>mdi-account</v-icon>
          <span class="caption text-lowercase">by person</span>
        </v-btn>
      </v-row>
      <v-card class="px-3 mb-5" v-for="project in projects" :key="project.title">
        <v-row :class="`pa-3 project ${project.status}`">
          <v-col cols="12" md="6">
            <div class="caption grey--text">Project title</div>
            <div>{{ project.title }}</div>
          </v-col>
          <v-col cols="6" sm="4" md="2">
            <div class="caption grey--text">Person</div>
            <div>{{ project.person }}</div>
          </v-col>
          <v-col cols="6" sm="4" md="2">
            <div class="caption grey--text">Due by</div>
            <div>{{ project.due }}</div>
          </v-col>
          <v-col cols="2" sm="4" md="2" class="d-flex align-center justify-center">
            <v-chip small :class="`${project.status} white--text caption`">
              {{ project.status }}
            </v-chip>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'dashboard',
  data() {
    return {
      projects: [
        { title: 'Design a new website', person: 'Carlos Wimmer', due: '1st Jan 2019', status: 'ongoing', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum quis possimus unde nihil illum harum maxime ex? Sed, dolor! Odio placeat iure totam voluptatum accusamus unde excepturi' },
        { title: 'Code up the homepage', person: 'Marcelo Lopes', due: '10th Jan 2019', status: 'complete', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum quis possimus unde nihil illum harum maxime ex? Sed, dolor! Odio placeat iure totam voluptatum accusamus unde excepturi repudiandae numquam?' },
        { title: 'Design video thumbnails', person: 'Edmar Hilário', due: '20th Dec 2018', status: 'complete', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum quis possimus unde nihil illum harum maxime ex? Sed, dolor! Odio placeat iure totam voluptatum accusamus unde Perferendis?' },
        { title: 'Create a community forum', person: 'Luiz Teixeira', due: '20th Oct 2018', status: 'overdue', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum quis possimus unde nihil illum harum maxime ex? Sed, dolor! Odio placeat iure totam voluptatum accusamus unde excepturi repudiandae numquam? Perferendis?' },
      ]
    }
  },
  methods: {
    sortBy (prop) {
      return this.projects.sort((a, b) => a[prop] < b[prop] ? -1 : 1) 
    }
  }
}
</script>

<style>
.project.complete {
  border-left: 4px solid #3cd1c2;
}
.project.ongoing {
  border-left: 4px solid orange;
}
.project.overdue {
  border-left: 4px solid tomato;
}
.v-chip.complete {
  background: #3cd1c2 !important;
}
.v-chip.ongoing {
  background: #ffaa2c !important;
}
.v-chip.overdue {
  background: #f83e70 !important;
}

</style>