<script>

   export default{
    props:{
        dettagli : Object,
    }
   
    }
   
        
    



</script>
<template>
      
        <div class="big-card">
          <div class="card">
            <img :src="dettagli.thumb" alt="sadasfsaf">
          </div >
          <h5>
            {{dettagli.series}}
          </h5>
        </div>
        
      
</template>

<style lang="scss" >
#comic-container{
  
   
    
    padding: 30px 0px;
    display: flex;
   
    h5{
      color: white;
      text-align: center;
      padding: 10px 0px;
      display: flex;
      flex-direction: column;
      &:hover{
        text-decoration: underline;
      }
     
    }
    .big-card{
      margin: 10px 10px;
      width: 14%;
      cursor: pointer;
      
    }
    .card{
      
        img{ 
          width: 100%;
        }
     
    }
    
    
  }
</style>
