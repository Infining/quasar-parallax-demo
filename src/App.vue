<template>
  <!-- Don't drop "q-app" class -->
  <div id="q-app">
    <q-window-resize-observable @resize="onWindowResize" />
    <q-parallax src="https://images.unsplash.com/photo-1506701234424-ef06760d8c8e?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=936e1dfe17a85554008d1fe1995f055" :height="windowHeight" :speed="1/2">
      <div slot="loading">Loading Image</div>
      <h1>Quasar Parallax</h1>
    </q-parallax>

    <div class="row justify-center items-center content">
      <div><h1>Flexbox</h1></div>
    </div>

    <q-parallax src="https://images.unsplash.com/photo-1483638906402-d942f4840969?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=bd2525da8a31727821f481da020c4b63" :height="windowHeight">
      <h1>Continued Image</h1>
    </q-parallax>
  </div>
</template>

<script>
/*
 * Root component
 */
import {
  QParallax,
  QWindowResizeObservable
} from 'quasar'

export default {
  data () {
    return {
      windowHeight: 0
    }
  },
  components: {
    QParallax,
    QWindowResizeObservable
  },
  methods: {
    onWindowResize (size) {
      this.windowHeight = size.height
    }
  }
}
</script>

<style lang="stylus">

.content
  height 50vh
  background #263238
  color #fff

</style>
