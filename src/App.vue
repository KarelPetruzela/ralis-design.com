<template>
    <router-view/>
</template>

<style lang="sass">

@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&family=Syne:wght@400;700&display=swap')

#app
    font-family: 'Inter', sans-serif
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    text-align: center
    color: white
    font-style: normal
    font-weight: 400

.font-syne
    font-family: 'Syne', sans-serif
    font-weight: 400

.font-inter
    font-family: 'Inter', sans-serif
    font-weight: 400

.font-weight-300
    font-weight: 300 !important


body
    background-image: url("assets/background.png")
    background-size: cover
    background-position-x: right
    background-position-y: top
    overflow-x: hidden

</style>
