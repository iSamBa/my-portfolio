<template>
  <div>
    <my-heading />
    <title-item title="Projects" />
    <projects-list />
    <title-item title="Contact" subtitle="me" />
  </div>
</template>

<script>
import ProjectsList from '~/components/ProjectsList.vue'
import TitleItem from '~/components/TitleItem.vue'
export default {
  components: { ProjectsList, TitleItem },
  head () {
    return {
      title: 'Aissam Bahou',
      meta: [
        { hid: 'description', name: 'description', content: 'I’m a robotics engineer and a self taught software developer' }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>

</style>
