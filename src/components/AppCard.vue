<script>
 export default{
    name:"AppCard",
    props:{
        image:String,
        title:String,
    },
    data(){
        return{
          
        }
    }
 }
</script>

<template>
    <div class="card">
        <img :src="image" alt="">
        <h3>{{ title }}</h3>

        
    </div>
</template>

<style scoped lang="scss">

img{
    width: 150px;
    height: 150px;
    background-color: aqua;
}
h3{
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
}

</style>