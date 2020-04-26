<template>
  <v-card flat>
    <div>
      <v-img :aspect-ratio="16/9" src="https://cdn.vuetifyjs.com/images/parallax/material.jpg">
      </v-img>
      <v-card flat>
        <v-img :aspect-ratio="1" src="http://b-ssl.duitang.com/uploads/item/201511/21/20151121171107_zMZcy.jpeg"
               width="80px" class="avator"></v-img>
        <v-card-text class="text-right">
          <p>XXXX</p>
        </v-card-text>
      </v-card>
      <v-divider></v-divider>
    </div>
    <v-list flat v-for="(item,n) in data" :key="n">
      <v-subheader>{{item.subtitle}}</v-subheader>
      <v-list-item
        :to="row.to"
        router
        exact
        v-for="(row,i) in item.children"
        :key="i"
      >
        <v-list-item-icon>
          <v-icon>{{row.icon}}</v-icon>
        </v-list-item-icon>
        <v-list-item-title>{{row.name}}</v-list-item-title>
      </v-list-item>
      <v-divider></v-divider>
    </v-list>
  </v-card>
</template>

<script>
    export default {
        name: "AppDrawerContent",
        data() {
            return {
                data: [
                    {
                        subtitle: '浏览',
                        children: [
                            {
                                icon: 'mdi-home',
                                name: '主页',
                                to: '/',
                            },
                            {
                                icon: 'mdi-bookmark-check',
                                name: '收藏',
                                to: '/favorite',
                            },
                            {
                                icon: 'mdi-animation',
                                name: '分类',
                                to: '/category',
                            },
                            {
                                icon: 'mdi-camera-iris',
                                name: '发现',
                                to: '/find',
                            },
                        ],
                    },
                    {
                        subtitle: '设置',
                        children: [
                            {
                                icon: 'mdi-account',
                                name: '个人中心',
                                to: '/account',
                            },
                            {
                                icon: 'mdi-cog',
                                name: '设置',
                                to: '/settings',
                            },
                        ],
                    },
                ]
            }
        }
    }
</script>
<style scoped>
  .avator {
    position: absolute;
    top: -40px;
    left: 5%;
    border: lightgray 2px solid
  }
</style>

<style scoped>

</style>
