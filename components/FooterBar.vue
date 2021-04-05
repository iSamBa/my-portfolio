<template>
  <footer v-observe-visibility="visibilityChanged" class="container-fluid" :class="visible">
    <div class="top">
      <span class="logo"><strong>Aissam</strong> Bahou</span>
    </div>
    <ul class="socials">
      <li><a href="https://www.twitter.com/isamba21/" target="_blank"><font-awesome-icon :icon="['fab', 'twitter']" /></a></li>
      <li><a href="https://www.github.com/isamba/" target="_blank"><font-awesome-icon :icon="['fab', 'github']" /></a></li>
    </ul>
    <small>&copy; Aissam Bahou {{ currentYear }}</small>
  </footer>
</template>

<script>
export default {
  name: 'FooterBar',
  data () {
    return {
      visible: 'visible'
    }
  },
  computed: {
    currentYear () {
      return new Date().getFullYear()
    }
  },
  methods: {
    visibilityChanged (isVisible, entry) {
      this.visible = isVisible ? 'visible' : ''
    }
  }
}
</script>
