<template>
  <div>
    <div class="container p-2">
      <div class="row py-5 g-5">
        <div class="col-5 py-5 d-flex flex-column justify-content-center">
          <h1 class="fw-bold">Distant learning for further expansion</h1>
          <p>Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process. </p>
          <button class="btn my-3"><i class="fas fa-download"></i>download free guide </button>
          <p>
            Have a question?
            <span>Get Free Sample <i class="fas fa-long-arrow-alt-right"></i> </span>
          </p>
        </div>
        <div class="col-7 position-relative text-center">
          <!-- Ciclo v-for per img background -->
          <img :src="element.img" alt="backgound photo profile" class="position-absolute" :class="element.class" v-for="(element, index) in bgProfile" :key="index + 'a'">

          <img src="@/images/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg" alt="photo profile" class="rounded-circle position-relative" id="photo-profile">
        </div>
        <div class="col-12 d-flex justify-content-around align-items-center">
          <!-- Ciclo v-for per img partner -->
          <img class="img-partner" :src="element.img" :alt="element.name" :class="element.class" v-for="(element, index) in partnerShip" :key="index + 'b'">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexJumbo',
  data: function(){
    return{
      bgProfile: [
        {
          img : require('@/images/maxcoach-shape-08.png'),
          class: 'f-bg'
        },
        {
          img : require('@/images/maxcoach-shape-08.png'),
          class: 's-bg'
        },
        {
          img : require('@/images/maxcoach-shape-07-150x150.png'),
          class: 't-bg'
        },
        {
          img : require('@/images/maxcoach-shape-02.png'),
          class: 'fo-bg'
        },

      ],
      partnerShip: [
        {
          img: require('@/images/client-logo-01.png'),
          name: 'style logo',
          class: 'my-partner-big'
        },
        {
          img: require('@/images/client-logo-02.png'),
          name: 'alberobello logo',
          class: 'my-partner-big'
        },
        {
          img: require('@/images/client-logo-03.png'),
          name: 'brook logo',
          class: 'my-partner-normal'
        },
        {
          img: require('@/images/client-logo-04.png'),
          name: 'pencil logo',
          class: 'my-partner-big'
        },
        {
          img: require('@/images/client-logo-05.png'),
          name: 'itsalive logo',
          class: 'my-partner-normal'
        },
        {
          img: require('@/images/client-logo-06.png'),
          name: 'sixbase logo',
          class: 'my-partner-small'
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/main-style.scss';
.col-5{
  h1{
    color: $GunPowder;
    font-size: 3rem;
  }
  p{
    color: $ShadyLady;
    font-weight: 700;
    span{
      color: $JungleGreen;
      border-bottom: 1px solid $ShadyLady;
    }
  }
  button{
    background-color: $JungleGreen;
    color: white;
    font-weight: 700;
    padding: .5rem 2rem;
    width: 280px;
    i{
      margin-right: 1rem;
    }
  }
}
.col-7{
  .f-bg{
    top: 40%;
    left: 0;
    transform: translateY(-40%);
  }
  .s-bg{
    left: 0;
    top: 70%;
    transform: translateY(-65%);
  }
  .t-bg{
    bottom: 0;
    right: 22%;
  }
  .fo-bg{
    right: 0;
    top: 25%;
    transform: translateY(-50%);
  }
  #photo-profile{
    z-index: 5;
  }
}
.col-12{
  .my-partner-big{
    height: 60px;
  }
  .my-partner-small{
    height: 25px;
  }
  .my-partner-normal{
    height: 35px;
    filter: brightness(110%);
  }
}
</style>
