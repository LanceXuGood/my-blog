<template>
  <div id="app">
    <v-app id="inspire">
      <v-toolbar color="white" fixed app>
        <v-toolbar-items>
          <v-btn v-for="(nav, key) in navs" :key="key" flat>{{nav.text}}</v-btn>
        </v-toolbar-items>
        <v-spacer></v-spacer>
        <v-toolbar-title right>
          <v-img
            :src="require('@/assets/logo.jpg')"
            class="mr-5 logo"
            contain
            height="48"
            width="48"
            max-width="48"
            @click="$vuetify.goTo(0)"
          />
        </v-toolbar-title>
      </v-toolbar>
      <v-content>
        <v-container fluid fill-height>
          <v-layout justify-center align-center>
            <nuxt-child/>
          </v-layout>
        </v-container>
      </v-content>
      <!-- <v-footer color="shades" app inset>
      <span class="white--text">&copy; 2017</span>
      </v-footer>-->
    </v-app>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navs: [
        {
          text: '前端技术',
          href: 'new'
        },
        {
          text: '游戏',
          href: 'breadcrumbs_link_1'
        },
        {
          text: '电影',
          href: 'breadcrumbs_link_2'
        }
      ]
    }
  }
}
</script>
<style style="css" >
.logo {
  border-radius: 50%;
}
</style>
