<script>

    export default{
        name:"AppMain",
        data(){
         return{
            message: "POWERED BY YARI"
         }
        },
        methods:{
         
          }
        }
    



</script>
<template>
<main>
  <div class="container">

    <h2>
        {{message}}
    </h2>
 
  </div>
</main>
</template>

<style lang="scss" >
main{
    background-color: black;
    height: 100px;
    h2{
        text-align: center;
        color: white;
        padding: 30px;
    }
}
</style>
