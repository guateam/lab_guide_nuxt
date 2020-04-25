<template>
    <v-card min-width="20vw">
      <v-card-text>
        <v-row no-gutters justify="center" align-content="center" v-for="(row,n) in data" :key="n">
          <v-col
            v-for="(item,i) in row"
            :key="i"
          >
            <v-card
              outlined
              tile
              class="text-center ma-2 pa-2"
              v-ripple

            >
              <v-card-text>
                <v-icon medium :color="item.color">{{item.icon}}</v-icon>
                <p>{{item.title}}</p>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
</template>

<script>
    export default {
        name: "AppDropPanel",
        data(){
            return {
                data:[
                    [
                        {
                            icon:'mdi-apps',
                            title:'title',
                            color:'red'
                        },
                        {
                            icon:'mdi-apps',
                            title:'title',
                            color:'green'
                        },
                        {
                            icon:'mdi-apps',
                            title:'title',
                            color:'blue'
                        },
                    ],
                    [

                    ]
                ]
            }
        }
    }
</script>

<style scoped>

</style>
