<template>
  <mainView />
</template>

<script>
import mainView from './view/mainView.vue'

export default {
  name: 'App',
  components: {
    mainView
  }
}
</script>

<style>
#app {
  font-family: 'nanumDahang';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

@font-face {
    font-family: 'nanumDahang';
    src: url('./fonts/나눔손글씨 다행체.ttf') format('truetype')
}
</style>
