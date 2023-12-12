
  
  <script>
  export default {
    name: "hero",
    props: {
      heroText: Array
    },
    data() {
      return {
        backgroundHero: "/src/img/jumbo-overlay.svg",
        imageHero: "/src/img/home-5-hero-image.png"
      };
    }
  };
  </script>


<template>
    <div class="background-beige">
      <div class="container-hero">
        <div class="container-big flex">
          <div class="container-text">
              <div v-for="content in heroText" :key="content">
                <h2>{{ content.title }}</h2>
                <p>{{ content.description }}</p>
                <button> <img :src="content.iconDownload"> {{ content.buttonText }} </button>
              </div>
          </div>
        
          <div class="container-imageHero">
            <img :src="imageHero">
          </div>
        </div>
        
        <img :src="backgroundHero" alt="Overlay" class="flipped-image">
      </div>
    </div>
  </template>
  
  <style scoped>
  .background-beige {
    height: 88vh;
  }
  
  .container-hero {
    position: relative;
    height: 88vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .flipped-image {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transform: scaley(-1);
  }
  h2{
    padding: 0;
    margin: 0;
    color: #3f3a64;
    font-size: 48px;
    margin-right: 100px;
    line-height: 1.17em;
  }
  p{
    font-size: 18px;
    color: #8C89A2;;
    font-weight: 300;
    line-height: 1.67em;
    margin: 30px 160px 30px 0px;
  }
  
  .container-text{
    width: 50%;
    
  }
  .container-imageHero{
    width: 50%;
    text-align: start;
  }
  .container-imageHero > img{
    width: 90%;
  
  }
  button{
    background-color: #20ad96;
    color: white;
    border: none;
    padding: 15px 40px 15px 40px;
    border-radius: 5px;
    font-size: 16px;
  }
  button > img{
    filter: invert(2);
  }
  </style>
  