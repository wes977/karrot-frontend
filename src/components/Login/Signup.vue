<template>
  <div>
      <div class="header">
        <img :src="loginImage"></img>
        <h4>Signup</h4>
      </div>
      <div class="content">
        <div class="white-box">
          <q-field icon="fa-user">
            <q-input v-model="name" float-label="Name"/>
          </q-field>
        </div>
        <div class="white-box" style="margin-top: 2em">
          <q-field icon="fa-envelope">
            <q-input v-model="email" float-label="Email"/>
          </q-field>
        </div>
        <div class="white-box">
          <q-field icon="fa-lock">
            <q-input v-model="password" type="password" float-label="Password"/>
          </q-field>
        </div>
        <div class="actions">
          <q-btn flat>Back to Login</q-btn>
          <q-btn class="submit shadow-4">Signup</q-btn>
        </div>
        <div style="clear: both"/>
      </div>
  </div>
</template>

<script>
import { QField, QInput, QBtn } from 'quasar'
import loginImage from '@/assets/people/cherry.png'

export default {
  components: { QField, QInput, QBtn },
  data () {
    return {
      loginImage
    }
  }
}
</script>

<style scoped lang="stylus">
@import '~variables'
.header
  padding 0.1em 1em
  img
    height 40px
    vertical-align middle
    margin-bottom: 20px
    margin-right: 10px
  img, h4
    display inline-block
  h4
    color $primary
.content
  border-radius 5px
  width 100%
  min-height 5em
  background-color $primary
  color white
  padding 1em 1em
  .white-box
    background-color white
    border-radius 2px
    padding .1em 1em
    margin-bottom .5em
    .q-field
      margin-top .2em
  .actions
    float right
    color $tertiary
    .submit
      color white
      background-color $secondary
    .submit:hover
      background-color $positive
</style>