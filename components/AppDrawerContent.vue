<template>
  <v-card flat>
    <div>
      <v-img :aspect-ratio="16/9" src="https://cdn.vuetifyjs.com/images/parallax/material.jpg">
      </v-img>
      <v-card flat>
        <v-img :aspect-ratio="1" src="http://b-ssl.duitang.com/uploads/item/201511/21/20151121171107_zMZcy.jpeg" width="80px" class="avator"></v-img>
        <v-card-text class="text-right">
          <p>XXXX</p>
        </v-card-text>
      </v-card>
      <v-divider></v-divider>
    </div>
    <v-list flat>
        <v-list-item
          to="/"
          router
          exact
        >
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>主页</v-list-item-title>
        </v-list-item>
    </v-list>
  </v-card>
</template>

<script>
    export default {
        name: "AppDrawerContent"
    }
</script>
<style scoped>
  .avator{
    position: absolute;
    top: -40px;
    left: 5%;
    border: lightgray 2px solid
  }
</style>

<style scoped>

</style>
