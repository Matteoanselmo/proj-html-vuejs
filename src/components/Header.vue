<template>
  <header>
    <div class="container p-2 d-flex align-items-center ">      
      <div class="row row-cols-auto align-items-center justify-content-between container-fluid p-0">
        <div class="col">
          <img class="img-logo" src="../images/dark-logo.png" alt="logo">
        </div>
        <div class="col">
          <ul class="d-flex m-0 align-items-center">
            <li v-for="(element, index) in searchBar" :key="index" class="px-3">
              <a href="#">
                {{ element }}
                <i class="fas fa-angle-down ms-1"></i>
                </a>
            </li>
            <li class="px-3">
              <a href="#">
                <i class="fas fa-user rounded-circle"></i> 
              </a>
            </li>
            <li>
              <div class="input-group">
                <input type="text" class="form-control" placeholder="Search..." >
                <span class="input-group-text" id="addon-wrapping">
                  <i class="fas fa-search"></i>
                </span>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'IndexHeader',
  data: function(){
    return{
    searchBar: ['Home' , 'Pages' , 'Courses' , 'Feautures' , 'Blog' , 'Shop']
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/main-style.scss';
header{
  
  .img-logo{
    width: 150px;
  }
  li{
    list-style: none;
    a{
      text-decoration: none;
      color: $Edward;
      i{
        font-size: smaller;
      }
    }
  }
  .input-group{
    width: 70%;
    input, span{
      background-color: $HintOfRed;
      border: none;
    }
    input{
      font-size: 1.2rem;
      font-weight: 600;
    }
    span{
      color: $MountainMeadow;
    }
  }
}
</style>
