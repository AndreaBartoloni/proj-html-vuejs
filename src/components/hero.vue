
  
  <script>
  export default {
    name: "hero",
    props: {
      heroText: Array
    },
    data() {
      return {
        backgroundHero: "/src/img/jumbo-overlay.svg"
      };
    }
  };
  </script>


<template>
    <div class="background-beige">
      <div class="container-hero ">
        <div class="container-big">
            <div v-for="content in heroText" :key="content">
                <h1>{{ content.title }}</h1>
                 <p>{{ content.description }}</p>
                <button><img :src="content.iconDownload"> {{ content.buttonText }}</button>
            </div>
        </div>
        
        <div >

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
  }
  
  .flipped-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transform: scaley(-1);
  }
  h1{
    padding: 0;
    margin: 0;
    color: #3f3a64;
  }
  button{

  }
  </style>
  