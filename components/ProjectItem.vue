<template>
  <div class="project">
    <img :src="imageUrl" alt="">
    <div>
      <h3>{{ title }}</h3>
      <p>{{ content }}</p>
      <a class="btn btn-lg btn-dark" :href="repoUrl" target="_blank"><font-awesome-icon :icon="['fab', 'github']" /> Github</a>
      <a class="btn btn-lg btn-primary" :href="webUrl" target="_blank"><font-awesome-icon :icon="['fab', 'chrome']" /> Live</a>
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

<style lang="
        scss"
        scoped
      >

</style>
      </font-awesome-icon></a>
    </div>
  </div>
</template>
