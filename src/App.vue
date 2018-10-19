<template  lang="pug">
  #app
    router-view
    //- tab(@tabChange="tabSwitch" :current="current")
</template>

<script>
import Tab from 'components/tab.vue'
export default {
  data () {
    return {
      current: 0
    }
  }
  // methods: {
  //   tabSwitch (index) {
  //     this.current = index
  //   }
  // },
  // components: {
  //   Tab
  // }
}
</script>

<style>
</style>
