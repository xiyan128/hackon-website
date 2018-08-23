<template>
  <div>
    <section>
      <v-parallax src="http://lc-yh97dhym.cn-n1.lcfile.com/631e0b84bdf74b30ded3.png" height="464">
        <v-layout column align-center justify-center class="white--text">
          <h1 class="white--text mb-2 display-2 text-xs-center font-weight-black">工作坊</h1>
          <div class="subheading mb-3 text-xs-center">专家助力，指点迷津</div>
          <v-btn class="red darken-3 mt-5" dark large nuxt to="/register">
            报名参赛即可免费参加
          </v-btn>
          <v-btn class="blue darken-3 mt-5" dark nuxt to="/register" disabled>
            观看视频「暂未开放」
            <v-icon right dark>theaters</v-icon>
          </v-btn>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout column wrap class="my-5" align-center>
        <v-flex xs12>
          <v-container grid-list-xl>
            <v-layout row wrap align-start>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="red--text text--darken-1 text--lighten-2">adjust</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">设立目的</div>
                  </v-card-title>
                  <v-card-text>
                    Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus
                    et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum
                    tincidunt. Suspendisse potenti.
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="yellow--text text--darken-1 text--lighten-2">help</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">如何参与</div>
                  </v-card-title>
                  <v-card-text>
                    Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus
                    et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum
                    tincidunt. Suspendisse potenti.
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="blue--text text--darken-2 text--lighten-2">info</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">研学主题</div>
                  </v-card-title>
                  <v-list class="transparent">
                    <v-list-tile>
                      <v-list-tile-action>
                        <v-icon class="blue--text text--lighten-2">code</v-icon>
                      </v-list-tile-action>
                      <v-list-tile-content>
                        <v-list-tile-title>Web 全栈开发 —— HTML5, CSS3, JS...</v-list-tile-title>
                      </v-list-tile-content>
                    </v-list-tile>
                    <v-list-tile>
                      <v-list-tile-action>
                        <v-icon class="blue--text text--lighten-2">explore</v-icon>
                      </v-list-tile-action>
                      <v-list-tile-content>
                        <v-list-tile-title>数据采集 —— Scrapy, PhantomJS...</v-list-tile-title>
                      </v-list-tile-content>
                    </v-list-tile>
                    <v-list-tile>
                      <v-list-tile-action>
                        <v-icon class="blue--text text--lighten-2">settings_input_component</v-icon>
                      </v-list-tile-action>
                      <v-list-tile-content>
                        <v-list-tile-title>Raspbarry Pi —— 开源硬件, Python...</v-list-tile-title>
                      </v-list-tile-content>
                    </v-list-tile>
                  </v-list>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>
    <section>
      <v-layout class="pb-5">
        <v-flex xs12 sm10 offset-sm1 lg10 offset-lg1>
        <v-select
          :items="Object.keys(sources)"
          label="选择视频"
          solo
          auto
          v-model="currentSource"
        ></v-select>
          <v-card :height="videoHeight">
              <video :src="sources[currentSource]" controls="controls" style="height: 100%; width: 100% "></video>
          </v-card>
        </v-flex>
      </v-layout>

    </section>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        sources: {
          'First': 'http://lc-yh97dhym.cn-n1.lcfile.com/ddd54950f1e6bf0f5e0e.mp4',
          'Second': 'http://lc-yh97DhYm.cn-n1.lcfile.com/7764e45f4290988da50d.mp4',
          'Third': 'http://lc-yh97DhYm.cn-n1.lcfile.com/cc77f1304f3047f15959.mp4',
          'Fourth': 'http://lc-yh97DhYm.cn-n1.lcfile.com/1cc8d1e0640b2c0ed1b5.mp4',
          'Fifth': 'http://lc-yh97DhYm.cn-n1.lcfile.com/417ff784468bc9434387.mp4'
        },
        currentSource: 'First'
      }
    },
    computed: {
      videoHeight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '220px'
          case 'sm': return '300px'
          case 'md': return '500px'
          case 'lg': return '600px'
          case 'xl': return '800px'
        }
      }
    }

  }
</script>