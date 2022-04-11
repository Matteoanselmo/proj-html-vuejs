<template>
  <div>
    <OnlineCourses/>
    <Tutoring class="bg-white"/>
    <TopLearners/>
    <BestBlog/>
  </div>
</template>

<script>
import Tutoring from './mainComponents/Tutoring.vue'
import OnlineCourses from './mainComponents/OnlineCourses.vue'
import TopLearners from './mainComponents/TopLearners.vue'
import BestBlog from './mainComponents/BestBlog.vue'
export default {
  name: 'IndexMain',
  components: {
    Tutoring,
    OnlineCourses,
    TopLearners,
    BestBlog
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
