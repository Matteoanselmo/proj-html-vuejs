<template>
  <div>
    <OnlineCourses/>
    <Tutoring class="bg-white"/>
    <TopLearners/>
  </div>
</template>

<script>
import Tutoring from './mainComponents/Tutoring.vue'
import OnlineCourses from './mainComponents/OnlineCourses.vue'
import TopLearners from './mainComponents/TopLearners.vue'
export default {
  name: 'IndexMain',
  components: {
    Tutoring,
    OnlineCourses,
    TopLearners
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
