<template>
  <div>
    <v-subheader>Dashboard</v-subheader>
    <v-container class="my-5">
      <v-card class="px-3">
        <v-row>
          <v-col cols="12" md="6">
            <div class="caption grey--text">Project title</div>
            <div>Create a new website</div>
          </v-col>
          <v-col cols="6" sm="4" md="2">
            <div class="caption grey--text">Person</div>
            <div>Carlos Wimmer</div>
          </v-col>
          <v-col cols="6" sm="4" md="2">
            <div class="caption grey--text">Due by</div>
            <div>1st May 2019</div>
          </v-col>
          <v-col cols="2" sm="4" md="2">
            <div class="caption grey--text">Status</div>
            <div>ongoing</div>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'dashboard'
}
</script>
