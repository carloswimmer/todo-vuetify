<template>
  <div class="home">
    <h1>Homepage</h1>
    
      <v-btn class="pink mx-3" dark>click me</v-btn>
      <v-btn depressed class="pink mx-3">click me</v-btn>
      <v-btn text color="pink" class="mx-3">click me</v-btn>
      <v-btn depressed class="pink mx-3" dark>
        <v-icon left>mdi-email</v-icon>
        email
      </v-btn>
      <v-btn small class="pink mx-3" dark>
        <v-icon small left>mdi-email</v-icon>
        email
      </v-btn>
      <v-btn large depressed class="pink mx-3" dark>
        email
        <v-icon right>mdi-email</v-icon>
      </v-btn>
      <v-btn fab small depressed class="purple mx-3" dark>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
  </div>
</template>

<script>
export default {
  name: 'home'
}
</script>

<style>
.home {
  margin: 15px;
}
</style>