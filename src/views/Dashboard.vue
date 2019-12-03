<template>
  <div>
    <v-subheader>Dashboard</v-subheader>
    <v-container class="my-5">
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
          <v-col cols="2" sm="4" md="2">
            <div class="caption grey--text">Status</div>
            <div>{{ project.status }}</div>
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

</style>