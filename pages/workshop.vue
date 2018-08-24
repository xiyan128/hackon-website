<template>
  <div>
    <section>
      <v-parallax src="http://lc-yh97dhym.cn-n1.lcfile.com/631e0b84bdf74b30ded3.png" :height="windowSize.y-64">
        <v-layout column align-center justify-center class="white--text">
          <h1 class="white--text mb-2 display-2 text-xs-center font-weight-black">工作坊</h1>
          <div class="subheading mb-3 text-xs-center">专家助力，指点迷津</div>
          <v-btn class="red darken-3 mt-5" dark large nuxt to="/register">
            报名参赛即可免费参加
          </v-btn>
          <v-btn class="blue darken-3 mt-5" dark @click="$vuetify.goTo('#videos')">
            观看录像
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
                    我们将聘请一些业界知名的讲师来为选手提供工作坊形式的培训。它可以为初学者解惑，使所有人都能接触到一些前沿的科技，胸有成竹地参加比赛。也能为大佬铺平通向「神级」的道路，探索更高级的技术。
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
                    参加无额外条件，无需费用，只需报参赛时勾上一个「有意向」的选项即可。若实在无法到达现场体验最佳的互动授课，我们还提供线上的回放，您可以随时观看。
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
                  <v-card-text>
                    主题一：<b>Arduino</b> <br> 一类便捷灵活、方便上手的开源电子原型平台，包含硬件 (各种型号的 arduino 板) 和软件 (arduino IDE)。她不仅适用于工程师进行快速原型开发，也同样适用于艺术家、设计师、爱好者和对于 “互动” 有兴趣的朋友们。同时他几乎是现代创客必备的工具。
                  </v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>
    <section id="videos">
      <v-layout>
        <v-flex xs12 sm10 offset-sm1 lg10 offset-lg1>
        <div class="headline text-xs-center" style="width:100%">视频回放</div>
        <div class="subheading pb-3 text-xs-center" style="width:100%">将会持续更新</div>
        <v-select
          :items="Object.keys(sources)"
          label="选择视频"
          hint="此处可以选择视频"
          solo
          v-model="currentSource"
        ></v-select>
        <video :src="sources[currentSource]" controls="controls" style="width: 100% "></video>
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
          '预告': 'http://lc-yh97dhym.cn-n1.lcfile.com/b744c891502befaeaf05.mov'
        },
        currentSource: '预告',
        windowSize: {
          x: 0,
          y: 0
        }
      }
    },
    methods: {
      onResize () {
        this.windowSize = { x: window.innerWidth, y: window.innerHeight }
      }
    },
    mounted () {
      this.onResize()
      // To refresh the page (not a decent approach )
      window.scrollTo(0, 1)
      window.scrollTo(0, 0)
    }

  }
</script>