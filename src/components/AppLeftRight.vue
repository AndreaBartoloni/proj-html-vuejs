
  
  <script>
  export default {
    name: "AppLeftRight",
    props: {
      items: Array,
    },
    data() {
      return {
        imgRigth: "/src/img/home-5-image-01.png",
        bgImgRigth: "/src/img/underlay-shape-grey.svg",
        title: "Learn At Your Own Pace",
        subtitle: "why hesitate to register",
      };
    },
  };
  </script>

<template>
    <div class="container-big">
      <div class="flex mt-120">
        <div class="container-right">
          <p>{{ subtitle }}</p>
          <h2>{{ title }}</h2>
          <div v-for="rightGroup in items.contentLeftRight" :key="rightGroup" class="mb-20">
            <div class="flex justify-content-between">
              <h6>{{ rightGroup.titleRight }}</h6>
              <div class="flex">
                <div v-for="rightItem in rightGroup.contentRight" :key="rightItem">
                  <img :src="rightItem.check">
                  <span>{{ rightItem.description }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="container-image-left">
          <img :src="bgImgRigth" class="absolute">
          <div class="relative">
            <img :src="imgRigth">
          </div>
        </div>
      </div>
    </div>
  </template>
  
<style scoped>
 h2{
    padding: 0;
    margin: 0;
    color: #3f3a64;
    font-size: 48px;
    margin-right: 100px;
    line-height: 1.17em;
    margin-bottom:40px;
    margin-top: 25px;
  }

  .container-right > p{
    font-size: 15px;
    text-transform: uppercase;
    color: #696969;
    letter-spacing: 2px;
}
.container-image-left{
    width: 50%;
    display: flex;
    align-items: center;
    text-align: center;
    margin-top: 120px;
}
.relative > img{
    width: 70%;
}
.relative{
    position: relative;
    width: 100%;
}
.absolute{
    position: absolute;
    width: 30%;
}
.container-right{
    width: 50%;
    margin-top: 120px;
}
.accordion-description{
    box-shadow: 0 15px 50px rgba(51, 51, 51, 0.1);
    padding: 20px 30px;
    border-radius: 5px;
    margin: 0;
}

h6{
    font-size: 18px;
    color: #696969;
    font-weight: 600;
    margin: 0;
    padding: 0;
}
</style>