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
              "current" :" false"
            },
            {
              "text": "COMICS",
              "url":"#",
              "current" :" true"
            },
            {
              "text": "MOVIES",
              "url":"#",
              "current" :" false"
            },
            {
              "text": "TV",
              "url":"#",
              "current" :" false"
            },
            {
              "text": "GAMES",
              "url":"#",
              "current" :" false"
            },
            {
              "text": "COLLECTIBLES",
              "url":"#",
              "current" :" false"
            },
            {
              "text": "VIDEOS",
              "url":"#",
              "current" :" false"
            },
            {
              "text": "FANS",
              "url":"#",
              "current" :" false"
            },
            {
              "text": "NEWS",
              "url":"#",
              "current" :" false"
            },
            {
              "text": "SHOP",
              "url":"#",
              "current" :" false"
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
          <a :class="{ active: link.current }" :href="link.url">
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
          padding-bottom: 15px;
        }
        & :hover,
        &.active {
          color: blue;
          border-bottom: 2px solid blue;
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
