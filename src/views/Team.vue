<template>
  <div>
    <v-container class="my-3">
      <v-row>
        <v-col cols="12" sm="6" md="4" lg="3" v-for="person in team" :key="person.name">
          <v-card class="mx-auto" max-width="344">
            <v-img :src="`https://cdn.vuetifyjs.com/images/cards/${person.bg}`" height="150px" class="text-center pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar" :alt="`foto de ${person.name}`" />
              </v-avatar>
            </v-img>

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
        { name: 'Carlos Wimmer', role: 'Web developer', avatar: '/avatar-1.png', bg: 'sunshine.jpg' },
        { name: 'Edmar Hilário', role: 'Graphic designer', avatar: '/avatar-2.png', bg: 'server-room.jpg' },
        { name: 'Luiz Teixeira', role: 'Web developer', avatar: '/avatar-3.png', bg: 'house.jpg' },
        { name: 'Marcelo Lopes', role: 'Social media maverick', avatar: '/avatar-4.png', bg: 'road.jpg' },
        { name: 'Caio da Silva', role: 'Sales guru', avatar: '/avatar-5.png', bg: 'plane.jpg' }
      ]
    }
  }
}
</script>
