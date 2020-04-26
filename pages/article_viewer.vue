<template>
  <v-layout
    justify-center
    align-center
  >
    <v-card max-width="99%" min-width="90%">
      <v-toolbar
        flat
      >
        <v-toolbar-title>Title</v-toolbar-title>
        <v-subheader>author:XXX</v-subheader>
        <v-spacer></v-spacer>

        <v-btn icon to="/article_history" >
          <v-icon>mdi-history</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-book-plus</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-toolbar>
      <v-divider></v-divider>
      <v-card-text>
        Test
      </v-card-text>
    </v-card>
  </v-layout>
</template>

<script>
    export default {
        layout:'detail_layout'
    }
</script>

<style scoped>

</style>
