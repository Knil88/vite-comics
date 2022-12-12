<script>

    export default{
        name:"AppHeader",
        data(){
         return{
          imageName:"dc-logo.png",
         }
        },
        methods:{
          getImage:function(imgPath){
            return new URL(imgPath, import.meta.url).href
          }
        }
    }



</script>

<template>
  <header>
    <img :src=" getImage(`../assets/img/${imageName}`)" alt="logo">
  </header>
</template>

<style lang="scss" scoped>


</style>
