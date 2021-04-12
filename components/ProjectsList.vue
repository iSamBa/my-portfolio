<template>
  <section id="projects" class="box-inner ">
    <div class="content">
      <project-item
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :content="project.content"
        :image-url="project.imageURL"
        :repo-url="project.repoURL"
        :web-url="project.webURL"
      />
    </div>
  </section>
</template>

<script>
import Projects from '@/store/projects'
import ProjectItem from './ProjectItem.vue'
export default {
  name: 'ProjectsList',
  components: { ProjectItem },
  computed: {
    projects () {
      return Projects
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
