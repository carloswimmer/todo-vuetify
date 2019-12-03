<template>
  <div>
    <v-subheader>Dashboard</v-subheader>
    <v-container class="my-5">
      <v-row  >
        <v-col cols="12" md="6">
          <v-btn outlined block color="primary">1</v-btn>
        </v-col>
        <v-col cols="4" md="2">
          <v-btn outlined block color="primary">2</v-btn>
        </v-col>
        <v-col cols="4" md="2">
          <v-btn outlined block color="primary">2</v-btn>
        </v-col>
        <v-col cols="4" md="2">
          <v-btn outlined block color="primary">2</v-btn>
        </v-col>
      </v-row>
      <v-row class="justify-space-around">
        <v-col cols="4" md="3">
          <v-btn outlined block color="success">1</v-btn>
        </v-col>
        <v-col cols="4" md="3">
          <v-btn outlined block color="success">2</v-btn>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'dashboard'
}
</script>
