<template>
  <v-container fluid fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 lg6 xl4>
        <v-card class="elevation-2">
          <v-toolbar dark color="red darken-3">
            <v-toolbar-title>报名比赛</v-toolbar-title>
          </v-toolbar>
          <v-card-text>
            <v-form ref="form" v-model="valid" lazy-validation>
              <v-text-field v-model="name" :rules="nameRules" :counter="10" label="真实姓名" required></v-text-field>
              <v-text-field v-model="school" :rules="schoolRules" label="学校" required></v-text-field>
              <v-text-field v-model="phoneNums" :rules="phoneRules" label="手机号" required></v-text-field>
              <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
              <v-text-field v-model="qq" :rules="[v => !!v || '请填写你的QQ号']" label="QQ"></v-text-field>
              <v-select v-model="role" :items="roles" :rules="[v => !!v || '请选择你的角色']" label="角色" required></v-select>
              <v-textarea auto-grow v-model="intro" label="个人简介" placeholder="eg：我擅长Android、iOS、web前后端开发，精通C++、Java、Python、汇编等语言。现役oi选手。" required></v-textarea>
              <v-checkbox v-model="workshop" label="有意向参加免费提供的工作坊？名额有限，抢完即止。" required></v-checkbox>
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-btn color="green" style="width:100%" @click.native="submit" :disabled="!valid">就这样</v-btn>
          </v-card-actions>
          <v-alert :value="error" type="error" class="subheading">报名失败，请向组委会寻求帮助！</v-alert>
          <v-alert :value="success" type="success" class="subheading">报名成功</v-alert>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  import axios from 'axios'

  export default {
    data: function () {
      return {
        valid: false,
        name: '',
        nameRules: [
          v => !!v || '务必填写你的名字',
          v => (v && v.length <= 10) || '我不信有这么长的名字'
        ],
        school: '',
        schoolRules: [
          v => !!v || '请填写你的学校'
        ],
        phoneNums: '',
        phoneRules: [
          v => !!v || '请填写你手机号码',
          v => /^[1][3,4,5,7,8][0-9]{9}$/.test(v) || '请写个像样点11位手机号码'

        ],
        email: '',
        emailRules: [
          v => !!v || '务必填写你的电子邮箱',
          v => /.+@.+/.test(v) || '请写个像样点的邮箱地址'
        ],
        qq: '',
        role: null,
        roles: [
          '程序员',
          '设计师',
          '产品经理',
          '其它'
        ],
        intro: '',
        workshop: false,
        error: false,
        success: false
      }
    },

    methods: {
      submit () {
        if (this.$refs.form.validate()) {
          this.error = false
          this.success = false
          // Native form submission is not yet supported
          axios.post('https://yh97dhym.api.lncld.net/1.1/classes/Applicant', {
            name: this.name,
            phoneNums: this.phoneNums,
            email: this.email,
            qq: this.qq,
            school: this.school,
            role: this.role,
            intro: this.intro,
            workshop: this.workshop
          }, {
            headers: {
              'X-LC-Id': 'yh97DhYmgEor03OJrptewIVs-gzGzoHsz',
              'X-LC-Key': 'jfrMVuUoTN7x8NomemFPQvBa',
              'Content-Type': 'application/json'
            }}).then(res => {
            if (res.status === 201) {
              this.success = true
              this.$refs.form.reset()
            } else {
              this.error = true
            }
          })
        }
      }
    }
  }
</script>