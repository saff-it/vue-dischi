<template>
  <div id="app">
    <spotiHeader />
    <spotiMain />
  </div>
</template>

<script>
import spotiHeader from './components/spotiHeader.vue'
import spotiMain from './components/spotiMain.vue'

export default {
  name: 'App',
  components: {
    spotiHeader,
    spotiMain,
  }
}
</script>


<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";

@import "./styles/general.scss";




</style>
