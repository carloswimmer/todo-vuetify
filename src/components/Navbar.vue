<template>
  <nav>
    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon class="grey--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">Todo</span>
        <span>Ninja</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text color="grey">
        <span>Sign Out</span>
        <v-icon right>mdi-exit-to-app</v-icon>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer dark clipped app v-model="drawer" color="#00b2cc">
      <v-list>
        <v-list-item>
          <v-list-item-avatar class="grey lighten-2">
            <v-img src="/avatar-1.png" alt="Picture of me"></v-img>
          </v-list-item-avatar>
        </v-list-item>
        <v-list-item link two-line>
          <v-list-item-content>
            <v-list-item-title class="title">Carlos Wimmer</v-list-item-title>
            <v-list-item-subtitle>cw@santos.sp.gov.br</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        <v-list-item v-for="item in items" :key="item.title" router :to="item.route" >
          <v-list-item-icon>
            <v-icon>
              {{ item.icon }}
            </v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>
              {{ item.title }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard', route: '/' },
        { title: 'My Projects', icon: 'mdi-folder', route: '/projects' },
        { title: 'Team', icon: 'mdi-account', route: '/team' }
      ]
    }
  }
}
</script>

<style>

</style>
