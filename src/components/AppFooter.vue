<script>
import { toValidAssetId } from '@vue/compiler-core';

  export default {
    name:'AppFooter',
    data(){
        return{
            navFooter:[
                        {
                          sectionTitle: "dc comics",
                          option:["Characters","Comics","movies","TV","games","videos","news"]
                        },
                        {
                          sectionTitle:"shop" ,
                          option:["shop DC","shop DC collectibles"]
                        },
                        {
                          sectionTitle: "dc",
                          option:["terms of us","privacy","add choice","advertising","jobs","subscriptions","talent","cpsc certificates","ratings","shop help","contact us"]
                        },
                        {
                          sectionTitle: "sites",
                          option:["DC", "mad magazine","DC kids"," DC universe","dc power visa"]
                        },
            ]
        }
    }
    
  }
</script>

<template>
<footer>
  <div class="footer-top">
    <div class="container">
      <div class="left">
        <section v-for="item in navFooter">
          <h2>{{item.sectionTitle}}</h2>
          <ul>
            <li v-for=" item2 in item.option">
              <a href="">{{item2}}</a>
            </li>
          </ul>
        </section>
        
      </div>
      <div class="right">
        <img src="../assets/img/dc-logo-bg.png" alt="">
      </div>
        
    </div>
  </div>

  <div class="footer-bottom">
    <div class="container">
      <button>sign-up now!</button>
      <div>
        <h2>follow us</h2>
        <ul>
          <li>
            <a href=""><img src="../assets/img/footer-facebook.png" alt=""></a>
          </li>
          <li>
            <a href=""><img src="../assets/img/footer-periscope.png" alt=""></a>
          </li>
          <li>
            <a href=""><img src="../assets/img/footer-pinterest.png" alt=""></a>
          </li>
          <li>
            <a href=""><img src="../assets/img/footer-youtube.png" alt=""></a>
          </li>
          <li>
            <a href=""><img src="../assets/img/footer-twitter.png" alt=""></a>
          </li>
        </ul>
      </div>

    </div>
  </div>
</footer>

</template>

<style scoped lang="scss">
@use "../style/mixins.scss" as *;
@use "../style/variables.scss" as *;

.footer-top{
  height: 300px;
  background-image: url(../assets/img/footer-bg.jpg);
  .container{
    position:relative;
@include display-flex(space-between,center,0);
        color: white;
        .left{
          @include display-flex(start,center,2rem);
          padding: $padding2;
          section{
       li{
        color: darkgray;
       }
       
      }

        }
    
      .right{
        width: 450px;
        position: absolute;
        top:-50px;
        right:3rem;
      }
  }
}
.footer-bottom{
  position: relative;
  z-index:10;
  background-color: rgb(36, 32, 32);
  height: $height100;
  padding: $padding2;
  .container{
    @include display-flex(space-between,center,0);
    ul{
      @include display-flex(space-between,center,1rem);

    }
    div{@include display-flex(space-between,center,1rem);
      h2{
        color: $bg-color-blue;
      }
    }
    button{
      display: inline-block;
      color:white;
      width: 100px;
      height: 2rem;
      background-color:  rgb(36, 32, 32);
      border:1.5px solid $bg-color-blue
    }
  }
}


</style>