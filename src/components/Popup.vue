<template>
  <v-dialog v-model="dialog" max-width="600">
    <template v-slot:activator="{ on }">
      <v-btn color="info" depressed dark v-on="on">Add new project</v-btn>
    </template>

    <v-card>
      <v-card-title class="headline grey lighten-3" primary-title>Add a New Project</v-card-title>

      <v-card-text>
        <v-form class="px-3">
          <v-text-field name="title" label="Title" id="title" v-model="title" prepend-icon="mdi-folder"></v-text-field>
          <v-textarea name="info" label="Information" id="info" v-model="content" prepend-icon="mdi-pencil"></v-textarea>

          <v-menu
            v-model="menu"
            :close-on-content-click="false"
            min-width="290"
          >
            <template v-slot:activator="{ on }">
              <v-text-field
                :value="dateFormatted"
                clearable
                label="Due date"
                prepend-icon="mdi-calendar-range"
                v-on="on"
                @click:clear="due = null"
              ></v-text-field>
            </template>
            <v-date-picker v-model="due" @change="menu = false"></v-date-picker>
          </v-menu>

        </v-form>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn color="success" depressed @click="submit">Add project</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
import moment from 'moment'

export default {
  data() {
    return {
      dialog: false,
      menu: false,
      title: '',
      content: '',
      due: new Date().toISOString().substr(0, 10)
    }
  },
  methods: {
    submit() {
      this.dialog = false
      // eslint-disable-next-line no-console
      console.log(this.title, this.content, this.due)
      this.title = ''
      this.content = ''
      this.due = new Date().toISOString().substr(0, 10)
    }
  },
  computed: {
    dateFormatted () {
        return this.due ? moment(this.due).format('Do MMM YYYY') : ''
      },
  }
}
</script>

<style>

</style>