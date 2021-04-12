<template>
  <div />
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
    imageURL: {
      type: String,
      required: true
    }
  }

}
</script>

<style lang="scss" scoped>

</style>
