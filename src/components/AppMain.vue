<script>
import { baseCompile } from '@vue/compiler-core';

  export default {
    name:'AppMain',
    data(){
        return{
         navMain:[
                  {
                    icona:"-digital-comics",
                    option:"digital comics",
                  },
                  {
                    icona:"-merchandise",
                    option:"DC merchandise",
                  },
                  {
                    icona:"-shop-locator",
                    option:"shop-locator",
                  },
                  {
                    icona:"-subscriptions",
                    option:"subscriptions",
                  },
                  {
                    icona:"-subscriptions",
                    option:"subscriptions",
                  },
         ]
         

        }
    },
    methods:{
      getImagePath: function(img){
        return new URL(`../assets/img/buy-comics${img}.png`, import.meta.url).href
      }
    }
    
  }
</script>

<template>
  <div class="main-top">
    <div class="container">
    -->content goes here &lt;--
    </div>
  </div>
  <div class="main-bottom">
    <div class="container">
      <ul>
        <li v-for=" item in navMain">
          <a href="">
            <!-- <img src="../assets/img/buy-comics-shop-locator.png" alt=""> -->
            <img :src="getImagePath(item.icona)" alt="">
            <span>{{ item.option }}</span>
          </a>
        </li>
      </ul>
    </div>
  </div>


</template>

<style scoped lang="scss">
@use "../style/variables.scss" as *;
@use "../style/mixins.scss" as *;
.main-top{
  background-color: black;
  color: white;
    .container{
      height: $height100;
      @include display-flex(start,center,0)
  
 }
} 
.main-bottom{
  position:relative;
  z-index:1;
  background-color:$bg-color-blue;
  .container{
    height: $height130;
    line-height: $height130;
    ul{
      color:white;
      @include display-flex(space-around,center,2rem);
      img{
      width: 2rem;
      vertical-align: middle;
      margin-right: 1rem;
   
    }
    }
    
  }
}



</style>