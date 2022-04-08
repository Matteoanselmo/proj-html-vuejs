<template>
  <div>
    <OnlineCourses/>
    <Tutoring class="bg-white"/>
    
  </div>
</template>

<script>
import Tutoring from './mainComponents/Tutoring.vue'
import OnlineCourses from './mainComponents/OnlineCourses.vue'
export default {
  name: 'IndexMain',
  components: {
    Tutoring,
    OnlineCourses
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
