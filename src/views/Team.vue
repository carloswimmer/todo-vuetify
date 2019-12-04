<template>
  <div>
    <v-subheader>Team</v-subheader>
    <v-container class="my-5">
      <v-row>
        <v-col cols="12" sm="6" md="4" lg="3" v-for="person in team" :key="person.name">
          <v-card class="text-center ma-3">
            <v-responsive class="pt-4">image goes here</v-responsive>
            <v-card-text>
              <div class="text-center subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn text small color="grey">
                <v-icon small left>mdi-message-text</v-icon>
                Message
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" sm="6" md="4" lg="3" v-for="person in team" :key="person.name">
          <v-card class="mx-auto" max-width="344">
            <v-img src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg" height="200px"></v-img>

            <v-card-title>{{ person.name }}</v-card-title>

            <v-card-subtitle>{{ person.role }}</v-card-subtitle>

            <v-card-actions>
              <v-btn text color="grey">
                <v-icon>mdi-message-text</v-icon>
                Message
              </v-btn>
            </v-card-actions>

          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'team',
  data() {
    return {
      team: [
        { name: 'Carlos Wimmer', role: 'Web developer' },
        { name: 'Edmar Hilário', role: 'Graphic designer' },
        { name: 'Luiz Teixeira', role: 'Web developer' },
        { name: 'Marcelo Lopes', role: 'Social media maverick' },
        { name: 'Caio da Silva', role: 'Sales guru' }
      ]
    }
  }
}
</script>
