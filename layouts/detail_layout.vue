<template>
  <v-app light>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <AppDrawerContent></AppDrawerContent>
    </v-navigation-drawer>
    <v-app-bar
      extended
      flat
      max-height="20vh"
      color="primary"
      dark
      prominent
    >
      <v-app-bar-nav-icon @click.stop="drawer=!drawer"></v-app-bar-nav-icon>
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
    <v-content
      style="margin-top: -10vh"
    >
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
    import AppDrawerContent from "../components/AppDrawerContent";
    import AppDropPanel from "../components/AppDropPanel";
    export default {
        components: {AppDropPanel, AppDrawerContent},
        data(){
            return {
                drawer:false,
                menu:false,
            }
        }
    }
</script>

<style scoped>

</style>
