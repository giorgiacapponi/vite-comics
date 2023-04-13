<script>
  export default {
    name:'AppHeader',
    data(){
        return{
            navHeader:["characters","comics","movies","tv","games","collectibles","videos","fans","news","shop"]
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
            <li v-for="item in navHeader">
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
            @include display-flex(space-between,center,1.5rem);
            color: rgb(38, 37, 37);
            a{
                text-transform: uppercase;
                font-size: 0.8rem;
            }
        }
    }
}



</style>