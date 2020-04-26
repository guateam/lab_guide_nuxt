<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <AppDrawerContent></AppDrawerContent>
    </v-navigation-drawer>
    <v-app-bar
      flat
      color="primary"
      dark
      prominent
      dense
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-message-text</v-icon>
      </v-btn>
      <v-menu
        v-model="menu"
        right
        offset-x
        offset-y
        offset-overflow
      >
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on">
            <v-icon>mdi-apps</v-icon>
          </v-btn>
        </template>
        <AppDropPanel></AppDropPanel>
      </v-menu>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import AppDropPanel from "../components/AppDropPanel";
import AppDrawerContent from "../components/AppDrawerContent";
export default {
    components: {AppDrawerContent, AppDropPanel},
    data () {
    return {
      drawer: false,
    }
  }
}
</script>
