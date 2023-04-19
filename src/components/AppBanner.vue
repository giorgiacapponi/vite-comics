<script>
export default{
props:{
    image:String,
}
}
</script>

<template>
<div class="banner">
    <img src="../assets/img/jumbotron.jpg" alt="">

</div>
</template>

<style scoped lang="scss">
.banner{
    height: 100px;
  
    img{
        width: 100%;
        height: 300px;
        object-fit:fill;
       
    }

}

</style>