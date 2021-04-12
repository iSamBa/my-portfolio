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
      <button v-if="loadMore" @click="loadMoreProjects">
        LoadMore
      </button>
    </div>
  </section>
</template>

<script>
import Projects from '@/store/projects'
import ProjectItem from './ProjectItem.vue'
export default {
  name: 'ProjectsList',
  components: { ProjectItem },
  data () {
    return {
      projects: [],
      totalProjects: 0,
      shownProjects: 0,
      loadMore: false
    }
  },
  mounted () {
    this.getProjects()
  },
  methods: {
    getProjects () {
      this.totalProjects = Projects.length
      if (Projects.length > 3) {
        this.loadMore = true
        this.shownProjects = 3
        this.projects = Projects.slice(0, 3)
      } else {
        this.projects = Projects
      }
    },
    loadMoreProjects () {
      const additional = Math.min(this.totalProjects - this.shownProjects, 3)
      this.shownProjects += additional
      if (this.shownProjects === this.totalProjects) {
        this.loadMore = false
      }
      this.projects = Projects.slice(0, this.shownProjects + additional)
    }
  }

}
</script>

<style lang="scss" scoped>

</style>
