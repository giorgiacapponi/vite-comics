<script>
  export default {
    name:'AppHeader',
    data(){
        return{
            navHeader:["characters","comics","movies","tv","games","collectibles","videos","fans","news","shop"],
            active:null,
        }
    },
    methods:{
        addActive(index){
    
    this.active=index
      }
     
    }
    
  }
</script>


<template>
<header>
    <div class="container">
        <a href="" class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </a>
        <ul>
            <li v-for="(item,index) in navHeader" :class="[active===index?'active':'']" @mouseenter="addActive(index)">
                <a href="">{{ item }}</a>
            </li>
        </ul>
    </div>
</header>
</template>



<style scoped lang="scss">
@use "../style/mixins.scss" as *;
@use "../style/variables.scss" as *;

header{
    height: $height100;
    .container{
        height:$height100;
    @include display-flex(space-between,center,0);
        .logo{
            display: inline-block;
            width: 70px;
        }
        ul{
            height: 100px;
           
            @include display-flex(space-between,center,1.5rem);
            color: rgb(38, 37, 37);
            li{
            line-height: 95px;
            margin: -5px;
           
                a{
                text-transform: uppercase;
                font-size: 0.8rem;
               
               
            }
            }
          
        }
    }
}



</style>