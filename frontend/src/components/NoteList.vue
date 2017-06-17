<template lang="pug">
  #app
    .card(v-for="note in notes")
      .card-header
        button.btn.btn-clear.float-right(@click="deleteNote(note)")
        .card-title {{ note.title }}
        .card-subtitle {{ convertDateToTimeAgo(note.created_at) }}
      .card-body {{ note.body }}
</template>


<script>
import { mapGetters } from 'vuex'
import prettydate from 'pretty-date'

export default {
  name: 'note-list',
  computed: mapGetters(['notes']),
  methods: {
    convertDateToTimeAgo (date) {
      return prettydate.format(new Date(date))
    },
    deleteNote (note) {
      console.log(this.notes)
      this.$store.dispatch('deleteNote', note)
    }
  },
  beforeMount () {
    this.$store.dispatch('getNotes')
  }
}
</script>

<style>
  header {
    margin-top: 50px;
  }
</style>
