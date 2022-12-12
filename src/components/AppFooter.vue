<script>

    export default{
        name:"AppFooter",
        data(){
         return{
            commercials:[
            {
              "text": " BUY COMICS",
              "url":"#",
              "image" :"buy-comics-digital-comics.png"
            },
            {
              "text": "DC MERCHANDISE",
              "url":"#",
              "image" :"buy-comics-merchandise.png"
            },
            {
              "text": "SUBCRIPTION",
              "url":"#",
              "image" :"buy-comics-subcriptions.png"
            },
            {
              "text": "COMIC SHOP",
              "url":"#",
              "image" :"buy-comics-shop-locator.png"
            },
            {
              "text": "DC POWER VISA",
              "url":"#",
              "image" :"buy-power-visa.png"
            },
           
            
          ]
         }
        },
        methods:{
            getImage: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
          }
        }
    }
    



</script>
<template>
<footer>
  <div class="container-blue">
        <div id="marketplace">
            <div class="commercialLink" v-for="element  in commercials">
                <img :src= "getImage(`/img/{{element.image}}`)" alt="">
               <a href="#" class="info">
                    DIGITAL COMICS
               </a>
            </div>
            
            
           
        </div>
  </div>
</footer>
</template>

<style lang="scss" >

    .container-blue{
        background-color: #0282f9;
        padding: 20px;
        #marketplace{
            display: flex;
            width: 75%;
            margin: auto;
            color: white;
            
            .commercialLink{
                display: flex;
                
                img{
                    width: 25%;
                }
                .info{
                    align-self: center;
                    margin: 0px 10px ;
                    text-decoration: none;
                    color: white;
                    &:hover{
                        text-decoration: underline;
                    }
                }
            }
        }
    }
</style>
