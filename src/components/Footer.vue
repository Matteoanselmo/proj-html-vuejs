<template>
  <div>
    <div class="container p-2 pt-5">
      <div class="row">
        <div class="col-6 mb-5" v-for="(address, index ) in addressInfo" :key="index + 'k'" >
          <h5 class="mb-4 fw-bold">Address</h5>
          <div id="address-info">
            <p>{{address.location}}</p>
            <p>{{address.phone}}</p>
            <p class="mb-4">{{address.mail}}</p>
            <i class="fab fa-facebook-square me-3 fs-4"></i>
            <i class="fab fa-twitter me-3 fs-4"></i>
            <i class="fab fa-instagram me-3 fs-4"></i>
            <i class="fab fa-linkedin me-3 fs-4"></i>
          </div>
        </div>
        <div class="col-3" >
          <h5 class="mb-4 fw-bold">Explore</h5>
          <div class="d-flex flex-column flex-wrap" id="explore-info">
            <a v-for="(info, index) in exploreInfo" :key="index + 'l'"> {{info}} </a>
          </div>
        </div>
        <div class="col-3" >
          <h5 class="mb-4 fw-bold">Information</h5>
          <div class="d-flex flex-column flex-wrap" id="information-info">
            <a href="#" v-for="(info, index) in informationInfo" :key="index + 'm'"> {{info}} </a>
          </div>
        </div>
        <div class="col-12 text-center p-5">
          <a href="#"><i class="fas fa-copyright"></i> 2020 Maxcoach. All Rights reserved</a>
        </div>
      </div>
      <a href="#" class="fs-1 p-4 text-white" id="return-to-top">
        <i class="fas fa-long-arrow-alt-up "></i>
      </a> 
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexFooter',
  data: function(){
    return{
      addressInfo: [
        {
          location: '382 NE 191st St #87394 Miami, FL 33179-3899',
          phone: '+1(305)547-9909 (9am - 5pm EST, Monday - Friday)',
          mail: 'suuport@maxcoach.com'
        }
      ],
      exploreInfo: [
        'Start here',
        'Blog',
        'About us',
        'Success story',
        'Courses',
        'Contact us'
      ],
      informationInfo: [
        'Membership',
        'Purchase guide',
        'Privacy policy',
        'terms of service'
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/main-style.scss';
#address-info{
  color: $Edward;
}
#explore-info{
  height: 150px;
  a{
    color: $Edward;
  }
}
#information-info{
  a{
    color: $Edward;
  }
}
.col-12{
  a{
    color: $Edward;
  }
}
#return-to-top{
  position: fixed;
  bottom: 2%;
  right: 2%;
  height: 80px;
  width: 80px;
  background-color: $JungleGreen;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  i{
    color: white;
  }
}
</style>
