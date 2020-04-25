<template>
  <v-app light>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <v-list>
        <v-list-item></v-list-item>
      </v-list>
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
        <v-icon>mdi-mail</v-icon>
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
        <v-card>
          <v-card-title>Title</v-card-title>
        </v-card>
      </v-menu>
    </v-app-bar>
    <v-content
      style="margin-top: -10vh;padding-left: 10%;padding-right: 10%;"
    >
      <v-container>
        <v-card>
          <v-toolbar
            flat
          >
            <v-toolbar-title>Title</v-toolbar-title>
            <v-subheader>author:XXX</v-subheader>
            <v-spacer></v-spacer>

            <v-btn icon>
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
            <nuxt />
          </v-card-text>
        </v-card>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
    export default {
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
