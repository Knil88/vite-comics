<script>

    export default{
        name:"AppFooter",
        data(){
         return{
            bigLogo:"/img/dc-logo-bg.png",
            footerElement: [
                {
                    title: 'DC COMICS',
                    listLink: [
                        {
                            text: 'Characters',
                            url: '#',
                            activeElement: true
                        },
                        {
                            text: 'Comics',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'Movies',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'TV',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'Games',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'Videos',
                            url: '#',
                            activeElement: false
                        },
                        {
                            text: 'News',
                            url: '#',
                            activeElement: false
                        },
                    ]
                }, {
                  title: 'DC',
                    listLink: [
                        {
                            text: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            text: 'Privacy policy (New)',
                            url: '#'
                        },
                        {
                            text: 'Ad Choises',
                            url: '#'
                        },
                        {
                            text: 'Adverting',
                            url: '#'
                        },
                        {
                            text: 'Jobs',
                            url: '#'
                        },
                        {
                            text: 'Subscription',
                            url: '#'
                        },
                        {
                            text: 'Talent Workshps',
                            url: '#'
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            text: 'Ratings',
                            url: '#'
                        },
                        {
                            text: 'Shop Help',
                            url: '#'
                        },
                        {
                            text: 'Contact Us',
                            url: '#'
                        },
                    ]
                }, {
                  title: 'SITES',
                    listLink: [
                        {
                            text: 'DC',
                            url: '#'
                        },
                        {
                            text: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            text: 'DC Kids',
                            url: '#'
                        },
                        {
                            text: 'DC Universe',
                            url: '#'
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#'
                        }]

                }, {
                    title: 'SHOP',
                    listLink: [
                        {
                            text: 'Shop DC',
                            url: '#'
                        },
                        {
                            text: 'Shop DC Collectivles',
                            url: '#'
                        },
                    ]
                },
                
            ],
            imgSocial: [
                {
                    img: 'img/footer-facebook.png',
                    link: '#'
                }, {
                    img: 'img/footer-twitter.png',
                    link: '#'
                }, {
                    img: "img/footer-youtube.png",
                    link: '#'
                }, {
                    img: "img/footer-pinterest.png",
                    link: '#'
                }, {
                    img: "img/footer-periscope.png",
                    link: '#'
                }],
            commercials:[
            {
              "text": " BUY COMICS",
              "url":"#",
              "image" :"/img/buy-comics-digital-comics.png"
            },
            {
              "text": "DC MERCHANDISE",
              "url":"#",
              "image" :"/img/buy-comics-merchandise.png"
            },
            {
              "text": "SUBCRIPTION",
              "url":"#",
              "image" :"img/buy-comics-subscriptions.png"
            },
            {
              "text": "COMIC SHOP",
              "url":"#",
              "image" :"/img/buy-comics-shop-locator.png"
            },
            {
              "text": "DC POWER VISA",
              "url":"#",
              "image" :"/img/buy-dc-power-visa.svg"
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
            <div class="commercialLink" v-for="commercial  in commercials">
                <img :src= "commercial.image" alt="">
               <a href="commercial.url" class="info">
                   {{commercial.text}}
               </a>
            </div>
            
            
           
        </div>
      
  </div>
  <div id="wrap-container">
    <div id="list-container">
      <ul v-for= "(element, index) in footerElement">
        <li class="titolo-li">
          {{element.title}}
        </li>
        <li v-for="link in element.listLink" class="">
          <a :href="link.url">
              {{ link.text }}
          </a>
      </li>
      </ul>
    </div>
    <div id="big-logo-container">
        <img :src=" bigLogo" alt="">
    </div>
  </div>
  <div id="final-container">
    <div id="flex-container">
      <div>
        <button>
          SIGN UP NOW
        </button>
      </div>
      <div id="icon-container">
        <h3>FOLLOW US</h3>
                
        <a  v-for="img in imgSocial"  :href="img.link">
            <img :src="img.img" alt="Social icon">
        </a>
      </div>
    </div>
  </div>
</footer>
</template>

<style lang="scss" >

    .container-blue{
        position: sticky;
        z-index: 10000;
        background-color: #0282f9;
        padding: 20px;
        margin-bottom: 35px;
        #marketplace{
            display: flex;
            justify-content: center;
            margin: auto;
            color: white;
            
            .commercialLink{
                display: flex;
                
                img{
                    max-width: 45px;
                }
                .info{
                    align-self: center;
                    display: inline-block;
                    margin: 0px 10px ;
                    text-decoration: none;
                    color: white;
                    min-width: 150px;
                    &:hover{
                        text-decoration: underline;
                    }
                }
            }
        }
    }
    footer{
      background-image: url(/img/footer-bg.jpg);
      background-size: cover;
     
      
    }
   
        #wrap-container{
         
          width: 80%;
          padding-bottom: 15px;
          margin: auto;
          display: flex;
          
          
          
       
          #big-logo-container{
          
            

            img{
              position: absolute;
              right: 10%;
              top: 32%;
            }
          }

          #list-container{
           
            width:37% ;
          
            display: flex;
            flex-wrap: wrap;

          }
          ul{
            list-style: none;
            padding-left: 20px;
           
          }
        }
        .titolo-li{
          color:white;
          margin-bottom: 5px;
        
        }
        a{
          color:#56504a;
          text-decoration: none;
          margin: 5px 0px;
        }
        #final-container{
          background-color: #303030;
          padding: 20px 0px;
          width: 100%;
          z-index: 1000;
          position: sticky;

          button{
            align-self: center;
            background-color: transparent;
            color: white;
            border: 1px solid  #13528e ;
            padding:10px;
            cursor: pointer;
            

          }

         
        }
        #icon-container{
          display: flex;
          a{
            margin: 5px 5px;
          }
          h3{
            align-self: center;
            margin-left: 5px;
            color: #13528e;
          }
        }
        #flex-container{
          width: 70%;
          margin: auto;
          display: flex;
          justify-content: space-between;
        }
        
    
</style>
