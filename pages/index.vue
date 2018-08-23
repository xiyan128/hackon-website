<template>
  <div>
    <section>
      <v-parallax src="http://lc-yh97dhym.cn-n1.lcfile.com/9f0d8420fa6331e43f4f.png" height="600">
        <v-layout column align-center justify-center class="white--text">
         <h1 class="white--text mb-2 display-2 text-xs-center font-weight-black">Hack_on</h1>
          <div class="subheading mb-3 text-xs-center">属于中学生的Hackathon，年轻极客们的狂欢</div>
          <v-btn class="red darken-3 lighten-2 mt-5" dark large nuxt to="/register">
            为梦想而参赛!
          </v-btn>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout column wrap class="my-5">
        <v-flex xs12 sm4 class="my-3">
          <div class="text-xs-center">
            <h2 class="headline">实践是锻炼实力的第一步</h2>
            <span class="subheading">
              24 小时撸一个项目，您可敢试试？
            </span>
          </div>
        </v-flex>
        <v-flex xs12>
          <v-container grid-list-xl>
            <v-layout row wrap align-start>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="green--text text--darken-1 text--lighten-2">school</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">赛前，工作坊助力</div>
                  </v-card-title>
                  <v-card-text>
                    除了最终的比赛，活动还包括赛前开设的工作坊。我们将聘请一些业界知名的讲师来为选手做赛前的培训。它可以为或许是初学者的你解惑，能接触到一些前沿的科技，胸有成竹地参加比赛。又或许能为原本就是大佬的你铺平通向「神级」的道路，确保你能在赛中稳拿名次。<a href="/workshop" class="blue--text">了解更多</a>
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="yellow--text text--darken-2 text--lighten-2">flash_on</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">赛中，专家全程支持</div>
                  </v-card-title>
                  <v-card-text>
                    本活动受到了浙江省科协的积极支持。届时，技术专家将全程在场为提供必要的技术支持，这也将是选手们学习进步的一大助力。本次 Hackathon 采用无命题制，将鼓励开发者从多角度去发挥来实现自己的创意，而专家的指点也必将使大家的创意变身为现实。
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="red--text text--darken-1 text--lighten-2">attach_money</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">赛后，惊人的奖励</div>
                  </v-card-title>
                  <v-card-text>
                    虽然这是一场纯公益的比赛，以友好的技术交流作为比赛的出发点，组委会仍以筹款和接受无偿赞助的方式积累了一笔客观的资金，除去必要的开销外将全部投入奖池，以奖励获奖的队伍。比赛末评委将选出一、二、三奖，具体名额和奖品待定，但绝不会亏待各位的努力。
                  </v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>

    <section>
      <v-parallax src="http://lc-yh97dhym.cn-n1.lcfile.com/2df1cc15396e13350fc5.png" height="380">
        <v-layout column align-center justify-center class="white--text">
          <div class="headline white--text mb-3 text-xs-center">与同龄的计算机精英们随机组队</div>
          <em>这可能是你和各校大佬们相识的第一步</em>
          <v-btn class="red darken-3 lighten-2 mt-5" dark large nuxt to="/register">
            为团队而战!
          </v-btn>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-container grid-list-xl>
        <v-layout row wrap justify-center class="my-5">
          <v-flex xs12 sm4>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">关于我们</div>
              </v-card-title>
              <v-card-text>
                我们来自杭州不同的高中，因为共同的热爱相聚在了一起。从比赛立项伊始，所有的联络、宣传、筹备等工作皆由我们独立、无偿地完成。Hack_on是杭州地区的第一个此类 Hackathon 活动。我们作为杭州地区的此类活动的开始，将以全心的努力付诸于比赛的准备--一切的一切都是为了比赛能如期举行、完满落幕。(所以求您<a href="/register" class="blue--text">参个赛</a>吧 Orz)
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm4 offset-sm1>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">联系我们</div>
              </v-card-title>
              <v-card-text>
                对于关于比赛的的任何疑问，我们随时待命，以诚相待。
              </v-card-text>
              <v-list class="transparent">
                <v-list-tile>
                  <v-list-tile-action>
                    <v-icon class="blue--text text--lighten-2">phone</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title>777-867-5309</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-list-tile>
                  <v-list-tile-action>
                    <v-icon class="blue--text text--lighten-2">place</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title>浙江, 杭州</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-list-tile>
                  <v-list-tile-action>
                    <v-icon class="blue--text text--lighten-2">email</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title>john@vuetifyjs.com</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
              </v-list>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </section>
  </div>
</template>
