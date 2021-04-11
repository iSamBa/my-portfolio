<template>
  <div>
    <my-heading />
    <projects-list />
  </div>
</template>

<script>
import ProjectsList from '~/components/ProjectsList.vue'
export default {
  components: { ProjectsList },
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
