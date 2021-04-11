<template>
  <div v-observe-visibility="visibilityChanged" class="title container-fluid" :class="visible">
    <div class="top">
      <span class="logo">
        <strong>{{ title }}</strong> {{ subtitle }}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TitleItem',
  props: {
    title: {
      type: String,
      required: true
    },
    subtitle: {
      type: String,
      required: false
    }
  },
  data () {
    return {
      visible: 'visible'
    }
  },
  methods: {
    visibilityChanged (isVisible, entry) {
      this.visible = isVisible ? 'visible' : ''
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
