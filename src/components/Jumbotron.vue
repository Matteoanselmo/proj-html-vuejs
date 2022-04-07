<template>
  <div>
    <div class="container p-2">
      <div class="row py-5">
        <div class="col-6">
          <h1>Distant learning for further expansion</h1>
          <p>Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process. </p>
          <button class="btn"><i class="fas fa-download"></i>download free guide </button>
          <p>
            Have a question?
            <span>Get Free Sample <i class="fas fa-long-arrow-alt-right"></i> </span>
          </p>
        </div>
        <div class="col-6 position-relative">
          <!-- Ciclo v-for per img background -->
          <img :src="`../images/${element.img}.png`" alt="backgound photo profile" class="position-absolute" :class="element.class" v-for="(element, index) in bgPofile" :key="index + 'a'">

          <img src="../images/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg" alt="photo profile" class="rounded-circle position-relative" id="photo-profile">
        </div>
        <div class="col-12"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexJumbo',
  data: function(){
    return{
      bgPofile: [
        {
          img : 'maxcoach-shape-08.png',
          class: 'f-bg'
        },
        {
          img : 'maxcoach-shape-08.png',
          class: 's-bg'
        },
        {
          img : 'maxcoach-shape-07-150x150.png',
          class: 't-bg'
        },
        {
          img : 'maxcoach-shape-02.png',
          class: 'f-bg'
        },

      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#photo-profile{
  z-index: 5;
}
</style>
