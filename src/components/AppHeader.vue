<script>

    export default{
        name:"AppHeader",
        data(){
         return{
          imageName:"dc-logo.png",
          links:[
            {
              "text": " CHARACTERS",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "COMICS",
              "url":"#",
              "Current" :" true"
            },
            {
              "text": "MOVIES",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "TV",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "GAMES",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "COLLECTIBLES",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "VIDEOS",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "FANS",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "NEWS",
              "url":"#",
              "Current" :" false"
            },
            {
              "text": "SHOP",
              "url":"#",
              "Current" :" false"
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
<header>
  <div class="container">

 
    <nav>
      <div id="img-container">
        <img src="img/dc-logo.png" alt="Logo DC">
      </div>
      <ul>
        <li  v-for="(link, index) in links" :key="index">
          <a :class="{ active: link.Current }" :href="link.url">
            {{ link.text }}
          </a>
        </li>
      </ul>
    </nav>
  </div>
</header>
</template>

<style lang="scss" >
header {
  margin: 10px 0;
  position: sticky;
   & .container {
    width: 80%;
    margin: auto;
    ul {
      display: flex;
      list-style: none;
      align-self: center;
      margin-left: 14%;
      & li {
        padding: 0 10px;
        & a {
          color: black;
          text-decoration: none;
          padding-bottom: 45px;
        }
        & :hover,
        &.active {
          color: blue;
          border-bottom: 3px solid blue;
        }
      }
    }
  }
}
nav{
  display: flex;
#img-container{
 img{
  width: 60%;
 }
}
}
</style>
