<template>
  <div class="box-inner project">
    <img :src="imageUrl" alt="">
    <div>
      <h1>{{ title }}</h1>
      <p>{{ content }}</p>
      <a :href="repoUrl">GitHub</a>
      <a :href="webUrl">Live demo</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectItem',
  props: {
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    },
    imageUrl: {
      type: String,
      required: true
    },
    repoUrl: {
      type: String,
      required: true,
      default: '#'
    },
    webUrl: {
      type: String,
      default: '#'
    }
  }

}
</script>

<style lang="scss" scoped>

</style>
