<template lang="pug">
div Album
  button(@click="goShow") Click Me
    div Sfdfdf
  router-view
</template>

<script>
export default {
  data () {
    return {
    }
  },
  methods: {
    goShow () {
      this.$router.push('/album/show')
    }
  },
  components: {
  }
}
</script>

<style scoped>
#page {
  padding-bottom: 50px;
}
</style>
