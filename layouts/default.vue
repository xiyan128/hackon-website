<template>

  <v-app dark>
    <v-toolbar fixed height="64">
      <v-toolbar-title class="font-weight-black"><nuxt-link to="/">Hack_on</nuxt-link></v-toolbar-title>
      <v-divider class="mx-3 hidden-sm-and-down" inset vertical></v-divider>
      <span class="subheading hidden-sm-and-down">中学生的 Hackathon · 杭州 · 2018 </span>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn class="red darken-4" flat nuxt to="register">
          参赛
        </v-btn>
        <v-btn flat nuxt to="workshop">
          工作坊
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <v-content style="padding-top: 64px !important">
      <nuxt />
    </v-content>

    <v-footer height="auto">
      <v-card flat tile class="grey darken-4 text-xs-center p mx-0" style="width:100%">
        <v-card-text>
          &copy;2018 —
          <strong>Hack_on 组委会</strong>,
          made by <strong>Xiyan Shao</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>
