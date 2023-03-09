<template>
  <div class="main">

      <section class="logo">
          <img src="../assets/logo.svg" alt="Ralis design">
      </section>

      <section class="intro">
          <h3 class="pre-title font-inter">Hi, there! My name is Ralitsa and I’m a graphic designer specializing in</h3>
          <h1 class="title font-syne">Logo, Brand and web design</h1>
          <h4 class="post-title font-inter">to learn more about me check my portfolio and cv below. </h4>
          <div class="buttons font-syne">
              <a href="/assets/stoykova-portfolio.pdf" target="_blank">
                  portfolio
              </a>
              <a href="/assets/stoykova-cv.pdf" target="_blank">
                  cv
              </a>
          </div>
      </section>

      <section class="get-in-touch">
          <h4 class="font-inter">Let’s get in touch!</h4>
          <div>
              <a :href="'mailto:'+email" class="contact-e font-syne" v-text="email"/>
          </div>
      </section>

      <section class="moto">
          <h3 class="font-syne">bringing your ideas to life with <br> a passionate touch</h3>
      </section>

      <footer>
          <div class="columns">
              <div v-for="col in footerData" class="col" :key="col[0]">
                <div class="key font-syne" v-text="col[0]"/>
                <div class="value font-inter font-weight-300" v-text="col[1]"/>
              </div>
          </div>
      </footer>

  </div>
</template>

<style lang="sass" scoped>

.logo
    top: 0
    left: 0
    position: absolute
    width: 100vw

    img
        margin-left: -80vw
        margin-top: 40px

.intro

    .pre-title
        margin-top: 248px
        font-size: 1.3vw //23px
        text-transform: uppercase

    .title
        margin-top: 64px
        font-size: 5vw

    .post-title
        font-size: 0.9vw // 16px
        text-transform: uppercase
        margin-top: 128px

.get-in-touch
    h4
        margin-top: 124px
        font-size: 1vw

    > div
        margin-top: 32px

    a
        font-size: 1.8vw // 32px
        color: white
        text-decoration: none
        transition-property: font-size
        transition-duration: 0.2s
        transition-timing-function: ease-in-out
        transition-delay: .1s

        &:hover
            text-decoration: underline
            font-size: 2vw

.buttons
    margin-top: 64px
    display: flex
    justify-content: center
    vertical-align: middle

    a
        transition-property: background-color
        transition-duration: 0.25s
        transition-timing-function: ease-in-out
        transition-delay: .1s
        color: white
        justify-content: center
        text-decoration: none
        font-size: 1.4vw // 20.5px
        border: 1.5px solid white
        margin: 0 1vw
        padding: 16px 0
        border-radius: 100px
        width: 141px

        &:hover
            background-color: rgba(255, 255, 255, 0.2)


.moto
    h3
        font-size: 3.6vw // 64px
        margin-top: 248px
    h4
        margin-top: 64px
        font-size: 1.3vw //23px
        text-transform: uppercase

footer
    margin-top: 248px
    margin-bottom: 130px

    .columns
        display: flex
        text-align: left
        flex-direction: row
        justify-content: center

        .col
            margin: 0 2.8vw

    .key
        font-size: 1.3vw //23px
    .value
        font-size: 1vw // 17px

@media (max-width: 900px)

    .main
        margin: 0 25px

    .logo img
        margin-left: -75vw
        margin-top: 20px
    .intro
        .pre-title
            margin-top: 148px
            font-size: 14px //23px
        .title
            margin-top: 32px
            font-size: 23px
        .post-title
            font-size: 12px
            margin-top: 48px
    .get-in-touch
        h4
            margin-top: 48px
            font-size: 14px
        > div
            margin-top: 4px
        a
            font-size: 24px
            &:hover
                text-decoration: underline
                font-size: 2vw
    .buttons
        margin-top: 48px
        a
            font-size: 14px
            margin: 0 1vw
            padding: 12px 0
            width: 100px
    .moto
        h3
            font-size: 18px
            margin-top: 64px
        h4
            margin-top: 12px
            font-size: 12px
    footer
        margin-top: 100px
        margin-bottom: 30px
        .columns
            justify-content: center
            flex-direction: column
            .col
                margin: 10px 2.8vw 0
                text-align: center
        .key
            font-size: 18px
        .value
            font-size: 14px

@media (min-width: 901px) and (max-width: 1200px)
    .intro
        .pre-title
            font-size: 14px
        .title
            font-size: 26px
        .post-title
            font-size: 12px
    .get-in-touch
        h4
            font-size: 14px
        > div
            margin-top: 4px
        a
            font-size: 24px
    .buttons a
        font-size: 14px
    .moto
        h3
            font-size: 24px
        h4
            font-size: 12px
    footer
        .key
            font-size: 18px
        .value
            font-size: 14px

</style>

<script lang="ts">

import {defineComponent} from 'vue';

const EMAIL = "info@ralis-design.com";
const CELL = "+420 736 513 973";

export default defineComponent({
    name: 'HomeView',
    data() {
        return {
            email: EMAIL,
            mobile: CELL,
        }
    },
    computed: {
        footerData() {
            return [
                ['Ralitsa Stoykova', 'Freelance Graphic Designer'],
                ['e-mail:', EMAIL],
                ['mobile:', CELL],
                ['location:', 'Prague, The Czech Republic'],
                ['ID (IČO):', '17479665'],
            ]
        }
    }
});

</script>
