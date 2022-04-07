<template>
  <header class="container bg-white p-2 d-flex align-items-center ">
    <div class="row row-cols-auto align-items-center justify-content-between container-fluid">
      <div class="col">
        <img class="img-logo" src="../images/dark-logo.png" alt="logo">
      </div>
      <div class="col">
        <ul class="d-flex m-0 align-items-center">
          <li v-for="(element, index) in searchBar" :key="index" class="px-1">
            <a href="#">
              {{ element }}
              <i class="fas fa-angle-down"></i>
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
              <span class="input-group-text" id="addon-wrapping">@</span>
            </div>
          </li>
        </ul>
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
  height: 5vh;
  .img-logo{
    width: 150px;
  }
  li{
    list-style: none;
    a{
      text-decoration: none;
      color: $CodGrey;
    }
  }
  .input-group{
    input, span{
      background-color: #aeadae;
      border: none;
    }
    span{
      color: $MountainMeadow;
    }
  }
}
</style>
